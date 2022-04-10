# Overview

The Cask SDK is a lower level API for interacting with the [Cask Protocol](https://www.cask.fi) using javascript.

For a simple to use, fully functional checkout widget, see the [Cask Widgets](https://github.com/CaskProtocol/cask-widgets) repository.

# Installation

```shell
npm install --save @caskprotocol/sdk

# OR

yarn add @caskprotocol/sdk
```

# Setup

```javascript
// require
const { CaskSDK } = require('@caskprotocol/sdk');

// modules
import { CaskSDK } from '@caskprotocol/sdk';
```

# Usage

## Static Utilities

The `CaskSDK` is both a constructor that creates a stateful instance to the set of Cask functionality as well as
a namespaced set of utilties and helpers. The namespaces are:

| Name                  |                                              Description                                               |
|-----------------------|:------------------------------------------------------------------------------------------------------:|
| CaskSDK.abi           |                                 Access the various Cask contract ABIs                                  |
| CaskSDK.chains        |                  Information about the various chains supported by the Cask protocol                   |
| CaskSDK.defaultChains | Contains the map of which chains are supported in the various enviroments (testnet, production, etc..) |
| CaskSDK.deployments   |         Contains the addresses of the Cask protocol contracts on a given environment and chain         |
| CaskSDK.environments  |                                       Cask protocol environments                                       |
| CaskSDK.units         |                    Utilities and constants that represent financial unit formatting                    |
| CaskSDK.contracts     |              Helpers to ethers.Contract instances of the various Cask protocol contracts               |
| CaskSDK.enc           |                                            Data encryption                                             |
| CaskSDK.ipfs          |                                          IPFS reading/writing                                          |
| CaskSDK.utils         |                                Low level utilties such as data encoding                                |


## Services

The instance returned from instantiating an instance of `CaskSDK` has a namedspaced set of services that are accessible from the top
level instance handle. The configuration passed to the `CaskSDK` constructor is shares across all the possible services. The list
below assumes you created an instance in the variable `cask`. The services are:

| Name                   |                                                        Description                                                        |
|------------------------|:-------------------------------------------------------------------------------------------------------------------------:|
| cask.vault             |                           Interact with the Cask vault such as depositing and withdrawing funds                           |
| cask.subscriptions     | Interact with the Cask subscriptions service such as creating a new subscription, canceling an existing subscription, etc |
| cask.subscriptionPlans |           Interact with the Cask subscription plans such as becoming a service provider, setting up plans, etc            |
| cask.events            |                       A service to register event listeners on the various Cask protocol contracts                        |
| cask.prices            |                                A service to efficiently get asset prices and user balances                                |


## Configuration

The top-level `CaskSDK` instance accepts a configuration object that is shared among all the provided services. This is also where
the blockchain connections are established including the read-only and read-write (for sending txns) and websockets (for event listeners)
are configured.

The top-level configuration keys are:

| Name         |                         Description                         |
|--------------|:-----------------------------------------------------------:|
| environment  | Which Cask environment to run in (testnet, production, etc) |
| connections  | Ethers/web3 connections for read, read/write and websockets |
| ipfs         |             Configure which IPFS service to use             |
| enc          |          Data encryption configuration (if using)           |
| events       |                Event listener configuration                 |
| prices       |                  Price feed configuration                   |
| defaultUnits |            Default unit formatting configuration            |


### environment

Configure which Cask protocol environment in which to interact.

The `environment` can be the value `CaskSDK.environments.TESTNET`, `CaskSDK.environments.PRODUCTION` or `CaskSDK.environments.DEVELOPMENT`.

### connections

`connections` has 3 sub-objects with keys `rpc`, `signer` and `ws` with the value being a map of Chain ID to provider/signer configurations.

The value for an `rpc` configuration can be a string of an http(s) URL or an instance of an ethers `Provider` such as `ethers.providers.JsonRpcProvider`.

The value for a `signer` configuration must be an ethers `Signer` such as an `ethers.Wallet`.

The value for a `ws` (websocket) configuration should be a string to a wss URL. The `ws` entries are only required if using the `events` service.

If desired, `rpc` can be omitted, and any read-only operations will be done via the `provider` associated with the `signer` instead.

If no `signer` is provided, the SDK will be limited to read-only actions.

Any service method that expects an `address` will use the `signer` instead, if the address is not supplied.

**Example:**

```json
connections: {
  rpc: {
    [CaskSDK.chains.POLYGON_MUMBAI.chainId]: process.env.MUMBAI_PROVIDER_URL,
    [CaskSDK.chains.AVAX_TESTNET.chainId]: process.env.FUJI_PROVIDER_URL,
  },
  signer: {
    [CaskSDK.chains.POLYGON_MUMBAI.chainId]: new ethers.Wallet(process.env.WALLET_PK, process.env.MUMBAI_PROVIDER_URL),
    [CaskSDK.chains.AVAX_TESTNET.chainId]: new ethers.Wallet(process.env.WALLET_PK, process.env.FUJI_PROVIDER_URL),
  },
  ws: {
    [CaskSDK.chains.POLYGON_MUMBAI.chainId]: process.env.MUMBAI_WEBSOCKET_URL,
    [CaskSDK.chains.AVAX_TESTNET.chainId]: process.env.FUJI_WEBSOCKET_URL,
  }
}
```


### ipfs

Configure where IPFS read and write operations are performed.

Keys are:

* `ipfsProvider` - Valid values are one from `CaskSDK.ipfs.providers.<PROVIDER>` and defaults to `CaskSDK.ipfs.providers.PINATA`.
* `ipfsGateway` - URL to IPFS gateway used for read operations.

Any additional configuration items are provider-specific.

**`PINATA` IPFS provider configuration**:

* `pinataApiKey` - Pinata API key
* `pinataApiSecret` - Pinata API secret

**Example:**

```json
ipfs: {
  pinataApiKey: process.env.PINATA_API_KEY,
  pinataApiSecret: process.env.PINATA_API_SECRET,
}
```

### enc

TODO...


### events

Configure the event listener.

Keys are:

* `enabled` - [true/false] - Enable/disable the event listener. Default is `false`.
* `debug` - [true/false] - Enable event debugging to console logging. Default is `false`.


### prices

Configure the price/balance service. To enable, configure the `interval`, and all assets in the Cask protocol vault will be
tracked. See the `cask.prices.balance()` and `cask.prices.usdPrice()` methods to read prices and balances.

Keys are:

* `walletAddress` - Address to perform balance checks on. If not supplied and a `signer` was supplied in the `connections`, the address will be detected from there.
* `interval` - Interval (in ms) in which to refresh prices/balances.
* `priceMaxAge` - Max age (in seconds) for valid price data. If set, and a read is performed on an asset and the last asset price was acquired more than `priceMaxAge` seconds ago, an exception will be raised.


## Units

Any method that accepts an amount or price accepts it with a suffix on the variable name with either:

* `Asset` - Amount is expected to be a string containing the full asset decimals per its ERC-20 configuration
* `Simple` - Expected to be a simple javascript floating point value, irrespective of the ERC-20 decimals.

For example, the `cask.vault.deposit()` method can accept either `amountSimple` or `amountAsset`.

Any method that returns a value can accept two input parameters of `units` and `unitFormat`. The `units` can be one of:

* `CaskSDK.units.SIMPLE` - Basic floating point representation of values
* `CaskSDK.units.ASSET` - String representation of values with the full decimals as defined by the ERC-20 asset.
* `CaskSDK.units.NUMERAL` - Formatted value using the javascript `numeraljs` package with a default format using abbreviations and 2 decimals.

And the `unitFormat` is dependent on the format type. For `CaskSDK.units.NUMERAL`, the valid parameters are:
* `format` - The `numeraljs` format to use to format the amount. The default can be found in `CaskSDK.units.DEFAULT_NUMERAL_FORMAT`.

**Example:**

```javascript
// deposit 25.75 USDC into vault
cask.vault.deposit({asset: 'USDC', amountSimple: 25.75});

// return balance is NumeralJS string with only one decimal and no abbreviation
const currentBalance = await cask.vault.balance({unit: CaskSDK.units.NUMERAL, unitFormat: {format: '0.0'}});
```

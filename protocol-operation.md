# Protocol Operation

## Overview

The cask protocol functions by asking consumers to deposit a certain amount of whitelisted ERC-20 stablecoins into the protocol smart contract (their metaphorical “cask”) which are used to pay for the ongoing subscription to one or more service providers. The minimum amount required to deposit is enough to cover one month’s active subscription fees, but depositing more will reduce how often the cask needs to be topped up. The cask dashboard and widget provides visual feedback of a suggested deposit amount based on a multiple of the consumer’s monthly active subscription fees.

Consumers can withdraw at any time and are never locked. In exchange for depositing funds and maintaining a balance, the consumers will get the following benefits:

* Not pay any gas fees for deposits and each recurring subscription payment. Gas fees for each individual payment at subscription renewal time is handled by the protocol.
* Earn yield on the deposited balances.
* Receive CASK token rewards in proportion to their deposit balance.

On a regular basis, the [keepers](/components.md#keeper-contracts) will service the protocol to trigger any payments on subscriptions that need to be renewed. When a payment is processed, a consumer’s deposit balance is reduced and the associated provider’s balance increases by the same amount, minus [protocol fees](/protocol-fees.md). Providers receive a discount on the fee based on their Fee-Reduction Staked balance. Revenue from the protocol is distributed to the DAO treasury and governance stakers.

Providers can withdraw their balance at any time but until it is withdrawn will have the following benefits:

* Earn yield on the held balance.
* Receive CASK token rewards in proportion to their balance.

## Cask Diagram

![Cask Diagram](<.gitbook/assets/cask_diagram.png>)

## Base Asset

In the Cask protocol, consumers can deposit any number of whitelisted stablecoins into their “cask”. Due to the slight variations in value of various stablecoins relative to each other, the protocol denominates all balances in the **Base Asset**. The base asset can be changed via governance in case of changes to the stablecoin ecosystem, and could be different on each chain the protocol is deployed, but initially will be the [MakerDAO](https://makerdao.com) **DAI** stablecoin which is widely available on multiple chains and aligns with the decentralized philosophy of the cask protocol. At the time of deposit by consumers and a withdrawal by providers, if the deposited coin or withdrawn token is other than the Base Asset, the exchange rate will be applied using Chainlink oracle price feeds. For withdrawals by providers, if the protocol does not have sufficient quantity of the requested token at withdrawal time, the protocol will swap some of its reserve assets to the desired coin at the current market exchange rate to fulfil the withdrawal.

## Reserve Assets

Deposits by consumers can come in the form of any of the whitelisted stablecoins and are stored in the treasury. The protocol reserves a minimum amount of this treasury - defined as a percentage of the outstanding balance payable to providers. This is called the **Vault Reserve Factor**. The remaining treasury balance is sent to the yield generation strategies.

**Example:**

If the protocol has deposits worth of 1,000,000 DAI (comprised of any ratio of the whitelisted depositable assets), and currently there are 125,000 DAI worth of held balances by providers, and the Vault Reserve Factor is set to **0.8**, the protocol would deposit 900,000 DAI into the yield strategies, and retain 100,000 DAI worth of the various stablecoins to handle withdrawals from providers.


## Yield Generation

The protocol uses its treasury, minus the Reserve Assets, to generate yield which is payable to both consumers and providers as well as to generate income to the protocol to pay for various expenses. Yield strategies are managed by governance and could utilize different strategies on different chains. Once a day the protocol will rebalance to ensure the Vault Reserve Factor is met in the treasury.

## Multi-Chain

The cask protocol is by nature a micropayments service and due to the nature of gas fees on Ethereum mainnet, the protocol is only economically viable on layer 2/side chains and other cost-efficient layer 1 EVM compatible chains. The Ethereum mainnet will hold the primary treasury, where the CASK token will be minted and bridges will be used to send CASK tokens to other chains to be used for protocol operation. Each chain will maintain its own treasury to store consumer deposits, held provider funds, and yield income. Proposals to governance will be used to handle occasional rebalancing of CASK tokens across chains.

When providers install the [Subscribe Widget](/components.md#subscribe-widget) on their website, they will be able to choose which chains they would like to support. The consumer will need to have deposited funds on one of the configured chains in order to subscribe to the provider’s services.

## Subsidized Gas Fees

The cask protocol aims to make adoption as simple as possible for consumers and maintain parity with the traditional billing systems. To this end, the protocol uses the token buybacks and/or community treasury to subsidize certain gas fees (up to a limit set by governance) such as when depositing funds or starting a new subscription. The rebate is paid in the equivalent value of CASK tokens based on the current market rate of the gwei/ETH to CASK price.

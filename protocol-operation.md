# Protocol Operation

## Overview <a href="#_9l9jxyd2nwsq" id="_9l9jxyd2nwsq"></a>

The cask protocol functions by asking consumers to deposit a certain amount of whitelisted ERC-20 stablecoins into the protocol smart contract (called the “cask wallet") which are used to pay for the ongoing subscription to one or more service providers. The minimum amount required to deposit is enough to cover one month’s active subscription fees, but depositing more will reduce how often the cask needs to be topped up - and in turn reducing gas fees and the risk they run out of funds to pay for active subscription fees. The cask dashboard and widget provides visual feedback of a suggested deposit amount based on a multiple of the consumer’s monthly active subscription fees.

In exchange for depositing funds into their cask wallet, the consumers will get the following benefits:

* Not pay gas fees for each recurring subscription payment - only depositing funds into the protocol. Gas fees for each individual payment at subscription renewal time is handled by the protocol as long as the consumer’s deposit balance is enough to cover the subscription payment.
* Earn yield on the deposited balance - with the ability to claim this yield at any time, or use it to top up their deposit. Yield APR is governed by the Cask DAO. The protocol utilizes defi protocols to generate yield which is split between yield for the consumer and revenue to offset gas fees.
* Consumers will receive CASK token rewards in proportion to their cask wallet balance.

Keepers will regularly service the protocol to trigger any subscription payments that need to be processed that day. When a payment is processed, a consumer’s balance is reduced and the associated provider’s cask wallet balance increases by the same amount, minus protocol fees. Providers earn a discount on [protocol fees](protocol-fees.md) based on how many CASK tokens they have staked.

Providers can claim their balance at any time but until it is claimed will have the following benefits:

* Providers will receive CASK token rewards in proportion to their unclaimed balance.
* Earn yield on the unclaimed balance. Yield APR is governed by the Cask DAO.
* When ready to claim, a single transaction harvests all funds from all  subscription payments, earned yield and earned CASK tokens. Providers can choose to receive their subscription funds denominated in any of the whitelisted ERC-20 stablecoins.

## Base Asset <a href="#_c8yfjtvt6kev" id="_c8yfjtvt6kev"></a>

In the Cask protocol, consumers can deposit any number of whitelisted stablecoins into their cask wallet. Due to the slight variations in value of various stablecoins relative to each other, the protocol denominates all deposited balances in the **Base Asset**. The base asset can be changed via governance in case of changes to the stablecoin ecosystem, and could be different on each chain the protocol is deployed, but initially will be the [MakerDAO](https://makerdao.com) **DAI** stablecoin which is widely available on multiple chains and aligns with the decentralized philosophy of the cask protocol.

At the time of deposit or withdraw by either consumer or provider, if the transferring asset is other than the base asset, the exchange rate will be applied using Chainlink oracle price feeds along with a slippage fee.

## Reserve Assets <a href="#_3qvglqz02xr7" id="_3qvglqz02xr7"></a>

Deposits by consumers can come in the form of any of the whitelisted stablecoins and are stored in the treasury. The protocol reserves a minimum amount of this treasury - defined as a percentage of the outstanding balance payable to providers. This is called the **Claim Reserve Factor.** The remaining treasury balance is sent to the yield generation strategies.

\
**Example:**

If the protocol has deposits worth of 1,000,000 DAI (comprised of any ratio of the whitelisted depositable assets), and currently there are 125,000 DAI worth of unclaimed balances by providers, and the Claim Reserve Factor is set to **0.8**, the protocol would deposit 900,000 DAI into the yield strategies, and retain 100,000 DAI worth of the various stablecoins to pay out claims from providers.

## Yield Generation <a href="#_n9h8f6mj0k3y" id="_n9h8f6mj0k3y"></a>

The protocol uses its treasury, minus the Reserve Assets, to generate yield which is payable to both consumers and providers as well as to generate income to the protocol to pay for various expenses. Yield strategies are managed by governance and could utilize different strategies on different chains. The protocol will regularly rebalance to ensure the Claim Reserve Factor is met in the treasury.

## Multi-Chain <a href="#_bjrvhsnpsomn" id="_bjrvhsnpsomn"></a>

The cask protocol is by nature a micropayments service and due to the nature of gas fees on Ethereum mainnet, the protocol is only economically viable on layer 2/side chains and other cost-efficient layer 1 EVM compatible chains. The Ethereum mainnet will hold the primary treasury, where the CASK token will be minted and bridges will be used to send CASK tokens to other chains to be used for protocol operation. Each chain will maintain its own treasury to store consumer deposits, claimable provider funds, and yield income. Proposals to governance will be used to handle occasional rebalancing of CASK tokens across chains.

When providers install the Subscribe Widget on their website, they will be able to choose which chains they would like to support. The consumer will need to have deposited funds on one of the configured chains in order to subscribe to the provider’s services.

## Subsidized Gas Fees

The cask protocol aims to make adoption as simple as possible for consumers and maintain parity with traditional billing systems. To this end, the protocol uses the token buybacks and/or community treasury to subsidize certain gas fees (up to a limit set by governance) such as when depositing funds or starting a new subscription. The rebate is paid in the equivalent value of CASK tokens based on the current market rate of the gwei/ETH to CASK price.

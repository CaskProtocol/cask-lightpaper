# Components

## Protocol Smart Contract

The cask protocol vault smart contract manages a cask wallet for both the consumer and provider. The subscription protocol smart contract ensures the payments are processed on the specified interval and for the duration of the minimum subscription period. The provider has no ability to trigger any charges directly and is only entitled to what is agreed upon in the recurring payment definition held on-chain. The consumer can cancel the payment agreement at any time. Each payment to the provider is on-chain and is available to be withdrawn instantly and is not at risk of chargebacks. A [protocol fee](protocol-fees.md) is charged by the smart contract to pay for protocol expenses and fund the treasury.

## Rewards Contract

The rewards contracts manage the delegation to yield strategies on the reserve asset balances and CASK token distribution to various LPs/stakers.

## Yield Strategy Contracts

The yield strategy contracts manage yield generation of the reserve asset funds and are allocated a percentage of the reserve assets per governance. Different chains will have different sources for yield.

## Governance Contracts

The governance contracts manage token vesting, treasury management (reserve rate and stablecoin rebalancing), token buybacks and protocol owned liquidity.

## Keeper Contracts

Cask uses Chainlink Keepers for protocol upkeep and part of the Cask protocol fees and yield go to pay for this service. The various upkeep needed for the protocol are:&#x20;

* In order to process future payments within a subscription, without human intervention, the smart contracts must be triggered externally periodically.
* Manage the yield strategies and claim reserve factor.

## Dashboard App

The Cask app is a dashboard that is available to both consumers and providers. Consumers can manage/top-up their deposit balance, claim yield and CASK token rewards, see a list of all their past and active subscriptions, payment history, and cancel active subscriptions. Providers can claim subscription funds and CASK rewards, see a list of active subscribers, manage subscription plans and associated settings. The app code is hosted on the IPFS network using an IPNS/ENS name for high availability and censorship resistance.

## Subscribe Widget

The subscribe widget is a javascript widget that providers can add to their website/web app that easily offers a “Subscribe with Crypto” button that handles all the web3 wallet interactions with the consumer. It handles the spending approval and establishment of the subscription - the provider does not need any knowledge of web3 programming nor interact with any on-chain smart contracts if they so choose. The widget is customizable via html5 attributes with default subscription settings established when defining the subscription plan (payment interval, cost per interval, currency, etc…). The subscription widget code is hosted on the IPFS network using an IPNS/ENS name for high availability and censorship resistance.

## Webhook Bridge

The webhook bridge is an optional component the provider can choose to run to make it easy to integrate the Cask protocol into their existing application, especially if it is desired to not have to learn and integrate web3 technology into their stack. The webhook bridge listens for smart contract events such as new subscriptions, successful/unsuccessful payments on a subscription or subscription cancellations and translates these into JSON webhook events that can be sent to their existing infrastructure. A docker image will be provided to ease the operational knowledge required to run the webhook bridge.

# Introduction

Cask is a decentralized non-custodial protocol for managing recurring payment agreements (subscriptions) between a
consumer and a provider in addition to generating yield on held funds. Cask provides both consumers and providers
greater assurances than traditional recurring payment processing systems. Consumers are not subject to providers being
able to charge them whenever and whatever amount as is possible in the current credit card-based system. Providers are
assured of instant payment settlement without the risks of chargebacks from consumers. Both of these improvements are
made possible by the Cask protocol smart contracts facilitating the recurring payment flow.

Providers are instantly provisioned in the system and start accepting payments immediately. No need for account
approval, or to have a bank account to receive payment funds. All that is needed is an Ethereum wallet. Payments will
initially support a well-known set of ERC-20 stablecoins (such as USDC, USDT, DAI). This list can be expanded via
governance. Real-time stablecoin conversions via [curve](https://curve.fi) or [balancer](https://balancer.fi) allow the
consumer to pay in any whitelisted stablecoin, and the provider can receive the payment in another.

The Cask/smart contract model also solves another major problem of legacy subscription payment systems: fraud. Because
of the traditional ‘pull’ model required to bill a consumer’s credit card, service providers and billing services have
become major targets for attack, and when infiltrated, those payment credentials can be used in many places. The Cask
smart contract model ensures service providers to be paid the specific amount of money for the subscription payment at a
predefined interval. Gone are the days where your payment information is leaked and used all over the Internet. Since
Cask does not have to invest massive amounts of capital into anti-fraud systems, it can operate much more efficiently.

Consumers have learned to use various tricks to work around the problems mentioned above, such as generating one-time
credit cards, but this puts the burden of a poorly designed system on the consumer. Cask is designed to be both user
friendly to consumers and capital efficient for providers - reducing friction and lowering the costs to run a recurring
payment network.

The operation of the protocol works by consumers depositing funds into the contract which are then used to pay for each
recurring payment of active subscriptions. In addition, the protocol rebates the gas fees when depositing funds and
signing up for new subscriptions. In exchange for holding a balance in the protocol, yield is earned on the balance. The
protocol acts as a combined checking and savings account - retaining liquidity by being usable to make one-time and
subscription payments on the held balance and generating meaningful savings yield all in one. Providers can withdraw any
outstanding balances owed to them from consumers, and while the funds are held in the protocol, yield is earned on the
funds.

Cask is designed to expand cryptocurrency payments for subscription services to the masses while providing meaningful
yield on balances held in the protocol. Infrastructure components are available to providers that are compatible with
existing web2 stacks, dramatically reducing the technical complexity to offer recurring cryptocurrency payments. For the
consumer, the out-of-the-box **“Subscribe With Crypto”** button is user-friendly and compatible with a number of
wallets, and allows them to manage all their cryptocurrency subscriptions from one place.

# NFT Subscriptions

The NFT subscription flow implements a recurring payment agreement between a consumer and a service provider. The service
provider can be a traditional web2/SaaS type business or could also be any creator, community, impact DAO or project
that sustains via a recurring flow of funds from its members. Subscriptions are represented as an NFT in the consumers
wallet and many of the properties of the NFT can be customized. Providers can also configure the NFT to be limited and
transferable which opens up unique web3 economic opportunities.

Service providers configure one or more plans with a specific interval, price, optional free trial period, and a number
of other settings. It is also possible to create several types of discounts. Traditional discount codes are supported in
addition to web3-native discounts that can be offered to consumers holding a specific balance of an ERC20 token or an NFT
from a specific collection.

The NFT subscription flow supports the following features:
* Customizable billing period (days, weeks, months, years)
* Free trial with configurable length up to 30 days
* Discounts, both traditional coupon codes and [web3 discounts](https://blog.cask.fi/introducing-automated-discount-triggers-based-on-on-chain-data-for-web3-e4b98c941f07)
* Secure data collection (metadata only readable by provider and current subscription holder) via SDK (soon via widget)
* Optional pause capability to allow consumers to temporarily suspend their service
* Optional transferability to allow consumers to transfer/sell their subscription via NFT marketplaces
* Optional limit on max number of active users per plan (ie, country club membership model)

There are a number of supporting components that work with the subscription flow:

## Subscribe Widget

The subscribe widget is a javascript widget that can add to the service provider or community website/web app that easily offers a
“Subscribe with Crypto” button that handles all the web3 wallet interactions with the consumer. It handles the spending
approval and establishment of the subscription - the provider does not need any knowledge of web3 programming nor
interact with any on-chain smart contracts if they so choose. The widget is customizable via html5 attributes with
default subscription settings established when defining the subscription plan (payment interval, cost per interval,
currency, etc…). The subscription widget code is hosted on the IPFS network using an IPNS/ENS name for high availability
and censorship resistance.

When providers install the widget, they will be able to
choose which chains they would like to support. The consumer will need to have deposited funds on one of the configured
chains in order to subscribe to the provider’s services.

## Webhook Bridge

The webhook bridge is an optional component the provider can choose to run to make it easy to integrate the Cask
protocol into their existing application, especially if it is desired to not have to learn and integrate web3 technology
into their stack. The webhook bridge listens for smart contract events such as new subscriptions,
successful/unsuccessful payments on a subscription or subscription cancellations and translates these into JSON webhook
events that can be sent to their existing infrastructure. A docker image is also availble to ease the operational
knowledge required to run the webhook bridge.

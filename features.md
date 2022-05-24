# Features

Cask supports the following features for the subscription capabilities.

## Billing Periods

Billing periods can be any number of the following units:

* Days
* Weeks
* Months
* Years

## Discounts (coming soon)

A set of discount codes can be supplied at subscription plan creation or later. The discount code itself is stored as a
hash on-chain such that it is not possible to learn of valid discount codes simply by looking at the smart contract data
on-chain. Discounts properties:

* Percentage amount of the discount
* Expire the discount after a certain timestamp
* Specify the max number of uses

## Free Trials

A subscription plan can have a specified number of free days/weeks/months/years.

## Upgrades/Downgrades (coming soon)

With or without prorated prices.

## Pausing

If a provider chooses, they can allow a subscription plan to be pausable by the consumer. While paused, the consumer
will incur no charges, and once unpaused, billing will resume as of the unpaused date.

## Data Collection (coming soon)

Customer data can be collected via the Subscribe Widget that is needed to provision a subscription on the provider’s
platform. This includes things like email, name, or other contact info. This data is encrypted by the Subscribe Widget
using the dag-jose/[EIP-2844](https://eips.ethereum.org/EIPS/eip-2844) protocol and stored off-chain in the IPFS network
with the CID of the data stored on-chain as part of the subscription metadata. The provider can then retrieve this data
from IPFS and decrypt it using their wallet private key.

## Refunds

A function on the smart contract will facilitate a refund from the provider to the consumer, using funds from the
provider’s held funds. If the provider does not have enough funds in the protocol for a full refund, they would need to
transact the refund outside of the Cask protocol - for example - simply send a payment directly from their wallet to the
consumer.

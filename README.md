# Introduction

Cask is a decentralized non-custodial protocol for automating the flow of money in web3. The Cask base layer
implements a job scheduling and queuing system that can handle many types of automated money flows. The foundation
is built using [Chainlink Keepers](https://docs.chain.link/docs/chainlink-keepers/introduction/) with flow-specific
contracts operating above.

Examples of flow types are subscription payments, [automated investing](/flow-types/autobuy.md),
recurring peer-to-peer payments with many more flow types not only possible but under
active development. Each flow type generally consists of a protocol contract that the user interacts with directly,
and a manager contract in which the keepers call to handle the recurring transaction processing. More complex flows
could have several contracts to implement more complex capabilities.

Flows can be funded either by depositing funds into the Cask protocol (called the Cask Wallet) or
directly from a web3 non-custodial wallet such as Metamask, Coinbase Wallet and  Trust Wallet. If using a personal
wallet, the allowance is carefully configured to balance the need to automatically allowing the processing flow payments
with the security of not asking for an unlimited approval. Currently, the Cask protocol only allows payments via
stablecoins. The list of supported stablecoins is chain-dependent and the list can be found on the
[production deployment](/deployments/production.md) page.

When funds are put into the Cask Wallet, they generate yield via yield strategies. The most basic yield strategy
is for funds to be sent to a yield aggregator such as [Yearn Finance](https://yearn.finance/) or
[Beefy Finance](https://beefy.finance/). Additional yield strategies will be developed over time.

All operational decisions such as which chains, what stablecoins to support, and yield strategy allocation are governed
by the [Cask DAO](cask-dao.md).

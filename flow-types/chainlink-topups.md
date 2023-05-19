# Chainlink Topups

Many [Chainlink](https://chain.link) services such as [Automation](https://chain.link/automation)
and [VRF](https://chain.link/vrf) require payment in LINK. Maintaining the
appropriate
balance of LINK for services has required that a project keep an adequate supply of LINK on hand, manually monitor
the balances, and then manually deposit additional LINK when needed. As projects grow in size, launch on multiple
chains, and deal with
fluctuations in demand, this process becomes increasingly more complex to manage. Chainlink Topups automate this process
by automatically buying LINK using stablecoins from either the project's Cask Wallet, or their project vault/treasury
wallet.
Projects no longer need to monitor and manage their LINK balance.

## Funding Types

Depending on the Chainlink service being used, Cask supports all Chainlink funding models:

**Subscription** — Users create a subscription account with Chainlink and pre-funding the balance with LINK tokens. When
a
contract requests a chainlink service, such as functions or VRF, the subscriber’s LINK is deducted from their available
balance. Cask
monitors the subscription LINK balance, and tops it up as needed.

**Direct Funding** — Contracts can pay with LINK directly when requesting resources. This method requires the calling
contract/wallet to
directly
fund the interaction with LINK. Cask monitors the contract/address LINK balance, and tops it up as needed.

## Setup

Chainlink Top-ups for Automation and VRF can be set up from the [Cask dApp](https://app.cask.fi)
or [Javascript SDK](https://docs.cask.fi/developer-docs/javascript-sdk). The process is as follows.

* **Set a funding source (Cask balance or personal wallet allowance)**. Top-ups rely on having an available funding
  source to
  perform the recurring transaction. Cask allows users to choose from one of the following funding methods: holding a
  balance in a Cask Wallet or setting an allowance in your Personal Wallet. With either method, money flows use
  stablecoins to avoid exposure to volatility. Cask is also integrated with Gnosis Safe, enabling projects to leverage
  the
  wallet’s multisig features.
* **Enter Automation or VRF details**. For Automation, enter a registry address and Upkeep ID. For VRF, enter a VRF
  coordination address and subscription ID. For VRF Direct funding, enter a contract address and optional custom ID.
  These
  values can be found on the Chainlink management portal for the specific service.
* **Set a minimum LINK balance and dollar amount to top-up**. The top-up amount is denominated in USDC. An example
  top-up
  could be to top-up your VRF subscription balance with $500 USDC worth of LINK when the LINK balance drops below 50
  LINK.
* **Cask monitors the on-chain LINK balance**. When a user’s Chainlink balance falls below the defined threshold (e.g.
  50
  LINK), Cask automatically uses funds from the user’s funding source to acquire LINK at the current market price and
  deposits it on behalf of the user into the specified Chainlink service. Each time the balance drops below the
  threshold,
  Cask initiates another top-up.


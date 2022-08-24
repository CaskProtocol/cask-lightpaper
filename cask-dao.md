# Cask DAO

The Cask protocol operates as a DAO and generates fees to pay member rewards as well as fund operations and expansion.
The Cask Protocol’s native token will be the **CASK** token. This token will be used to govern the protocol, offer discounts to
providers who stake as well as distribute protocol revenue to governance stakers.

## Governance

During the initial launch of the protocol, the DAO will be governed by a multi-sig wallet held by the founding team.
Governance will be transitioned to governance token stakers over time as governance and decision making directly affects
participants of the network.

Once governance is transferred to the DAO, voting will use the gasless snapshot tool with voting weight calculated based
on governance-staked CASK tokens.

The following are some of the actions that are managed by the governance process:

* Smart contract upgrades
* Change ENS/IPNS to point to new hash for app upgrades
* Change ENS/IPNS to point to new hash for subscription widget upgrades
* Set whitelisted ERC-20 tokens allowed to be used for payments and payouts
* Mange yield strategies for protocol TVL (minus the reserve balance)
* Allocate treasury funds
* Elect multi-sig members
* Token burns
* Emergency shutdown

The following are protocol-level parameters that can be adjusted via governance:

* **Base Fees**: Payment fees (both fixed fee and min/max fee percentages) taken from payments to providers based on
  their balance in the [Fee Reduction Staking](/tokenomics.md#token-and-staking) contract.
* **Min Fee**: Minimum payment fee for the transaction, if the payment fee would be lower than this amount based on
  the Base Fees.
* **Min Payment**: The smallest payment value possible for a transaction.
* **Stake Target Factor**: Target number of **CASK** tokens a provider should stake in
  the [Fee Reduction Staking](/tokenomics.md#token-and-staking) contract per subscriber, per payment if they want to pay
  the minimum fee on the payment transaction.
* **Token Emissions**: Amount of **CASK** token reward emissions to liquidity providers and consumers/providers based on
  their deposit balances.
* **Yield Performance Fee**: Percentage fee subtracted from yield generation before passing through to
  consumers/providers.
* **Protocol Fee Distribution**: Percentage of protocol fee distribution between the protocol treasury
  and [Governance Stakers](/tokenomics.md#token-and-staking).
* **Vault Reserve Factor**: The multiple of assets to keep on hand in the protocol to handle anticipated
  consumer/provider withdrawals, with the remainder of the balance delegated to the yield strategies. If the vault does
  not have funds in the vault at the time of the withdrawal, a harvest from the yield strategy is performed inside the
  withdrawal transaction, so participants are never locked out of withdrawing their funds.

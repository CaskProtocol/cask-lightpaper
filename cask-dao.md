# Cask DAO

The Cask protocol operates as a DAO and generates fees to pay member rewards as well as fund operations and expansion. The Cask Protocol’s native token is the **CASK** token. This token is used to govern the protocol, offer discounts to providers who stake as well as distribute protocol revenue to governance stakers.

## Governance

During the initial launch of the protocol, the DAO will be governed by a multi-sig wallet held by the founding team. Governance will be transitioned to governance token stakers over time as governance and decision making directly affects participants of the network.

Once governance is transferred to the DAO, voting will use the gasless snapshot tool with voting weight calculated based on governance-staked CASK tokens.

The following are some of the actions that are managed by the governance process:

* Smart contract upgrades
* Change ENS/IPNS to point to new hash for app upgrades
* Change ENS/IPNS to point to new hash for subscription widget upgrades
* Set whitelisted ERC-20 tokens allowed to be used for payments and payouts
* Mange yield strategies for protocol TVL (minus the reserve balance)
* Set the Base Asset stablecoin of the protocol
* Allocate treasury funds
* Elect multi-sig members
* Token burns
* Emergency shutdown

The following are protocol-level parameters that can be adjusted via governance:

* **Base Fees**: Payment fees (both fixed fee and min/max fee percentages) taken from payments to providers based on their balance in the [Fee Reduction Staking](#token-and-staking) contract.
* **Stake Target Factor**: Target number of **CASK** tokens a provider should stake in the [Fee Reduction Staking](#token-and-staking) contract per subscriber, per payment if they want to pay the minimum fee on the payment transaction.
* **Token Emissions**: Amount of **CASK** token reward emissions to liquidity providers and consumers/providers based on their deposit balances.
* **Yield Performance Fee**: Percentage fee subtracted from yield generation before passing through to consumers/providers.
* **Protocol Fee Distribution**: Percentage of protocol fee distribution between the protocol treasury and [Governance Stakers](#token-and-staking).
* **Vault Reserve Factor**: The multiple of assets to keep on hand in the protocol to handle anticipated consumer/provider withdrawals, with the remainder of the balance delegated to the yield strategies. If the vault does not have funds in the vault at the time of the withdrawal, a harvest from the yield strategy is performed inside the withdrawal transaction, so participants are never locked out of withdrawing their funds.

## Token and Staking

The **CASK** token is used to govern the protocol, offer discounts to providers, and reward those holding balances in the protocol.

There are two staking options for CASK holders:

**Governance Staking** - CASK holders who stake their CASK into the governance staking contract will be able to propose and vote on DAO proposals and other governance activities as outlined above. These stakers also receive a share of the [Protocol Fees](/protocol-fees.md).

**Fee-Reduction Staking** - Providers who [stake](/protocol-fees.md#fee-reduction-staking) their CASK tokens are given a discount on protocol fees as detailed in the [Protocol Fees](/protocol-fees.md) section.

## Tokenomics

* Initial Circulating Supply: 130,000,000
* Total Supply: 1,000,000,000

![Final Distribution At 5 Years - 1B Tokens](<.gitbook/assets/cask_final_distribution.png>)

Emission/Vesting Schedule and Breakdown (in millions):

|                        |         |         |         |         |         |           |
| ---------------------- |---------|---------|---------|---------|---------|-----------|
| **Year**               | **0**   | **1**   | **2**   | **3**   | **4**   | **5**     |
| Team                   | 0       | 50      | 100     | 150     | 200     | 200       |
| Investors / Advisors   | 0       | 57      | 113     | 170     | 170     | 170       |
| Public LBP             | 30      | 30      | 30      | 30      | 30      | 30        |
| Community Treasury     | 100     | 150     | 200     | 250     | 300     | 350       |
| Staking Rewards        | 0       | 50      | 100     | 150     | 200     | 250       |
|                        |         |         |         |         |         |           |
| **Circulating Supply** | **130** | **337** | **543** | **750** | **900** | **1,000** |

**Team** - Vesting: 1 year cliff for 25%, remaining vests linearly over 3 years.

**Investors/Advisors** - Vesting: 1 year cliff for 33%, remaining vests linearly over 2 years.

**Liquidity Bootstrapping Pool** - Vesting: none.

**Community Treasury** - Vesting: 28% available immediately, remaining vests linearly over 5 years.

**Staking Rewards** - Vesting: none, released linearly over 5 years.

![Token Supply Schedule](<.gitbook/assets/cask_circulating_supply.png>)

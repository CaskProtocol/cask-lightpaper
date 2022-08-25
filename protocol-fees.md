# Protocol Fees

The Cask protocol charges the provider a fee on each payment to fund the treasury for protocol operations as well as to
generate fee distributions to governance stakers. The fee charged is set per blockchain based primarily on the gas fees
required to operate on the blockchain and is set by the Cask DAO governance process. and protocol fees are calculated
using a price denominated in the Base Asset of the protocol.

The current production fees are always available on the [Production Deployments](/deployments/production.md) page.

## Fee Reduction Staking

Protocol fees can be reduced by staking CASK tokens. The fee is weighted based on the interval of the subscription plan,
since more frequent payments require more upkeep by the protocol.

## Fee Formula

Definitions:

**Minimum Payment Value** = Minimum allowable value to be transacted for a payment, denominated in the Base Asset.

**Transaction Fee Rate Min** = Lowest possible fee rate charged by the protocol assuming the provider is staking the
optimal amount of CASK tokens.

**Transaction Fee Rate Max** = The fee rate charged by the protocol if no CASK tokens are staked by the service provider.

**Minimum Transaction Fee** = The lowest possible fee charged by the protocol regardless of the fee rates or staking, so
ensure the protocol earns enough to cover gas costs. Denominated in the Base Asset.

**Stake Target Factor** = Initially set to 100 (set by governance)

**Total Staked** = Number of CASK token staked by provider

**Subscriber Count** = Number of active subscribers to the subscription plan

**Subscription Plan Days** = Number of days between the subscription payments. For example, monthly subscriptions would
be $$365 \over 12$$(or 30.416), weekly subscriptions would be **7**, every two weeks would be **14** and quarterly would
be $$365 \over 12 * 3$$(or 91.25).

Fee Rate Formula:

$$
Fee Rate = Transaction Fee Rate Max -
$$
$$
(Transaction Fee Rate Max * \frac{Total Staked}{Subscriber Count * Stake Target Factor * \frac{365}{Subscription Plan Days}})
$$

**Example:**

Provider has 1,000 monthly subscribers on a plan paying 20 USDC/month and is staking 300,000 CASK. The chain has a
**Transaction Fee Rate Min** fee of 1%, and a **Transaction Fee Rate Max** fee of 2%.

The fee discount is calculated as:

**Load Factor** = $$365 \over Subscription Plan Days$$= 12

**Load Factor** = $$365 \over 365 \div 12$$= 12

**Min Fee Target** = $$Subscriber Count * Stake Target Factor * Load Factor$$= 1,200,000

**Min Fee Target** = $$1,000 * 100 * 12$$= 1,200,000

**Fee Discount Rate** = $$Total Staked \over Min Fee Target$$= 25 %

**Fee Discount Rate** = $$300,000 \over 1,200,000$$= 25 %

**Fee Rate** =$$Transaction Fee Rate Max - (Transaction Fee Rate Max * Fee Discount Rate)$$= 1.50 %

**Fee Rate** =$$2 \% - (2 \% * 25 \%)$$= 1.50 %

**Adjusted Fee Rate** = $$max(Transaction Fee Rate Min, Fee Rate)$$= 1.50 %

**Adjusted Fee Rate** = $$max(1 \%, 1.50 \%)$$= 1.50 %

**Applied Fee** = $$(Adjusted Fee Rate * Subscription Value)

**Applied Fee** = $$(1.50 \% * 20 USDC)$$= 0.30

As long as the **Applied Fee** is at least the **Minimum Transaction Fee**, no additional fee is added.

So with the monthly subscription value of 20 USDC, the applied fee would have been 0.40 USDC for the subscription 
payment, but with a 25% discount on this fee because the provider is staking 300,000 CASK, they would only pay a fee
of 1.50%, or 0.30 USDC per subscription payment.

Providers have 2 ways of reducing their fees: stake more CASK, or offer longer subscription intervals (ex: quarterly
instead of monthly).

## Yield Performance Fee

In addition to payment fees, the protocol also takes a percentage of yield generated from the various strategies. Just
like payment fees, the yield performance fee is split between the DAO treasury and CASK governance stakers.

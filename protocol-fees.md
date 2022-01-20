# Protocol Fees

The Cask protocol charges the provider a max fee of up to 2% (set by governance) of each payment to fund the treasury for protocol operations as well as to generate fee distributions to governance stakers. All subscription amounts and protocol fees are calculated using a price denominated in the [Base Asset](protocol-operation.md#base-asset) of the protocol.

## Fee Reduction Staking <a href="#_8kzti3jffff" id="_8kzti3jffff"></a>

Protocol fees can be reduced down from the max fee, to a minimum of 1% (set by governance) by staking CASK tokens. The fee is weighted based on the interval of the subscription plan, since more frequent payments require more upkeep by the protocol.

## Fee Formula

Definitions:

**Base Fixed Fee** = Initially set to 0 DAI (set by governance)

**Base Rate Fee Min** = Initially set to 1% (set by governance)

**Base Rate Fee Max** = Initially set to 2% (set by governance)

**Stake Target Factor** = Initially set to 100 (set by governance)

**Total Staked** = Number of CASK token staked by provider

**Subscriber Count** = Number of active subscribers to the subscription plan

**Subscription Plan Days** = Number of days between the subscription payments. For example, monthly subscriptions would be **** $$365 \over 12$$(or 30.41), weekly subscriptions would be **7**, every two weeks would be **14** and quarterly would be $$365 \over 12 * 3$$(or 91.25).

Fee Rate Formula:

$$
Fee Rate = Base Rate Fee Max   -
$$
$$
(Base Rate Fee Max * \frac{Total Staked}{Subscriber Count * Stake Target Factor * \frac{365}{Subscription Plan Days}})
$$

**Example:**

Provider has 1,000 monthly subscribers on a plan paying 20 DAI/month and is staking 300,000 CASK. The fee discount is calculated as:

**Load Factor** = $$365 \over Subscription Plan Days$$= 12

**Load Factor** = $$365 \over 365 \div 12$$= 12


**Min Fee Target** = $$Subscriber Count * Stake Target Factor * Load Factor$$= 1,200,000

**Min Fee Target** = $$1,000 * 100 * 12$$= 1,200,000


**Fee Discount Rate** = $$Total Staked \over Min Fee Target$$= 25 %

**Fee Discount Rate** = $$300,000 \over 1,200,000$$= 25 %


**Fee Rate** =$$Base Rate Fee Max - (Base Rate Fee Max * Fee Discount Rate)$$= 1.50 %

**Fee Rate** =$$2 \% - (2 \% * 25 \%)$$= 1.50 %


**Adjusted Fee Rate** = $$max(Base Fee Rate Min, Fee Rate)$$= 1.50 %

**Adjusted Fee Rate** = $$max(1 \%, 1.50 \%)$$= 1.50 %


**Applied Fee** = $$(Adjusted Fee Rate * Subscription Value) + Base Fixed Fee$$= 0.30

**Applied Fee** = $$(1.50 \% * 20 DAI) + 0$$= 0.30

So with the monthly subscription value of 20 DAI and a max base fee of 2%, the applied fee would have been 0.40 DAI for the subscription payment, but with a 25% discount on this fee because the provider is staking 300,000 CASK, they would only pay a fee of 1.50%, or 0.30 DAI per subscription payment.

Providers have 2 ways of reducing their fees: stake more CASK, or offer longer subscription intervals (ex: quarterly instead of monthly).

## Yield Performance Fee

In addition to payment fees, the protocol also takes a percentage of yield generated from the various strategies. Just like payment fees, the yield performance fee is split between the DAO treasury and CASK governance stakers.

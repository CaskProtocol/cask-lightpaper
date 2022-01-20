# Protocol Fees

The Cask protocol charges the provider a base fee of 1% (set by governance) of each payment in the currency of the payment to fund the treasury for staking rewards, upkeep, and community initiatives. This fee can be reduced by staking CASK tokens. The fee is weighted based on the interval of the subscription plan, since more frequent payments require more upkeep by the protocol.

All subscription amounts and protocol fees are calculated using a price denominated in the Base Asset of the protocol.

Definitions:

**Base Fixed Fee** = Initially set to 0.25 DAI (set by governance)

**Base Rate Fee** = Initially set to 1% (set by governance)

**Stake Target Factor** = Initially set to 100 (set by governance)

**Total Staked** = Number of CASK token staked by provider

**Subscriber Count** = Number of active subscribers to the subscription plan

**Subscription Plan Days** = Number of days between the subscription payments. For example, monthly subscriptions would be **** $$365 \over 12$$(or 30.41), weekly subscriptions would be **7**, every two weeks would be **14** and quarterly would be $$365 \over 12 * 3$$(or 91.25).

Fee Rate Formula:

$$
Fee Rate = Base Fee - (Base Fee * \frac{Total Staked}{Subscriber Count * Stake Target Factor * \frac{365}{Subscription Plan Days}})
$$

**Example:**

Provider has 1,000 monthly subscribers and is staking 300,000 CASK. The fee discount is calculated as:

**Load Factor** = $$365 \over 365 \div 12$$= 12

**No Fee Target** = $$1,000 * Stake Target Factor * Load Factor$$= 1,200,000

**Fee Discount Rate** = $$300,000 \over No Fee Target$$= 25 %

**Fee Rate** =$$Base Rate Fee - (Base Rate Fee * Fee Discount Rate)$$ = 0.75 %

**Total Fee** = $$(Fee Rate * Subscription Value) + Base Fixed Fee$$&#x20;

So assuming the monthly subscription value of 20 DAI, the Total Fee would be 0.45 DAI per subscription, but with a 25% discount on the Base Rate Fee, the provider staking 300,000 CASK would only pay a Total Fee of 0.40 DAI for the same subscription payment.

Providers have 2 ways of reducing their fees: stake more CASK, or offer longer subscription intervals (ex: quarterly instead of monthly).

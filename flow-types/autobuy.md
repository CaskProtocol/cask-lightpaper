# Auto Buy

Also known as **DCA** or Dollar Cost Averaging.

Automatically buy a specific amount of value (denominated in USDC) of a number of given assets on a regular basis. Auto-buys are completely
decentralized and assets are acquired via decentralized exchanges (dexes). Purchased assets are sent directly
to your personal wallet (even if using the cask wallet to fund the buys). Cask uses [Chainlink Oracles](https://data.chain.link/) 
to compare the current asset price in order to ensure the swapped quantity does not result in excess slippage.

The Cask DAO curates which assets are available for auto-buys on each chain based on the availability of tokens, 
on-chain liquidity and the reputation of the asset. 

Auto-buys have the following features:

* Choose the USDC amount and interval for automatic purchases
* Choose the max slippage allowed from the current Chainlink reported asset price
* Optionally set a maximum amount of value to invest over the lifetime of the auto-buy
* Optionally set a min and/or max price you are willing to pay for the asset - purchases are skipped if the asset price is outside the configured range

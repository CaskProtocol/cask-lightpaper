# Contract Description

| contract name          |                                                                     Description                                                                     |
|------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------:|
| CaskVault              |                                               Cask vault to store the various assets in the protocol                                                |
| CaskSubscriptions      | Cask subscriptions contract for subscription management. Implements ERC-721 for subscriptions to be represented as an optionally transferrable NFT. |
| CaskSubscriptionPlans  |                                        Cask subscriptions plans contract where the provider profile is held.                                        |
| CaskSubscriptionManager |                                   Processes subscription renewals and holds the subscription protocol parameters.                                   |


# Polygon

## Polygon Contracts

| contract name             |                                                          Address                                                          |
|---------------------------|:-------------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://polygonscan.com/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff)  |
| CaskSubscriptions         | [0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0](https://polygonscan.com/address/0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0)  |
| CaskSubscriptionPlans     | [0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e](https://polygonscan.com/address/0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e)  |
| CaskSubscriptionManager   | [0xfA07af9E5835D720b3798a37f716749252F94D71](https://polygonscan.com/address/0xfA07af9E5835D720b3798a37f716749252F94D71)  |


## Polygon Supported Stablecoins

| Coin  |                             Address                                                                                          |
|-------|:----------------------------------------------------------------------------------------------------------------------------:|
| *USDC |    [0x2791bca1f2de4661ed88a30c99a7a9449aa84174](https://polygonscan.com/token/0x2791bca1f2de4661ed88a30c99a7a9449aa84174)    |
| USDT  |    [0xc2132d05d31c914a87c6611c10748aeb04b58e8f](https://polygonscan.com/token/0xc2132d05d31c914a87c6611c10748aeb04b58e8f)    |
| DAI   |    [0x8f3cf7ad23cd3cadbd9735aff958023239c6a063](https://polygonscan.com/token/0x8f3cf7ad23cd3cadbd9735aff958023239c6a063)    |

 *= Base Asset

## Polygon Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys

| Name                    |   Value   |
|-------------------------|:---------:|
| Minimum Buy Amount      | 5.00 USDC |
| Transaction Fee         |   0.6 %   |
| Minimum Transaction Fee | 0.50 USDC |
| Minimum Period          |   1 Day   |
| Minimum Slippage        |   0.5 %   |
| Stake Target Factor     |    N/A    |


### Peer to Peer Transfers

| Name                |   Value   |
|---------------------|:---------:|
| Transaction Fee     | 0.50 USDC |
| Stake Target Factor |    N/A    |


# Avalanche

## Avalanche Contracts

| contract name            |                                                         Address                                                          |
|--------------------------|:------------------------------------------------------------------------------------------------------------------------:|
| CaskVault                |  [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://snowtrace.io/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff)   |
| CaskSubscriptions        |  [0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0](https://snowtrace.io/address/0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0)   |
| CaskSubscriptionPlans    |  [0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e](https://snowtrace.io/address/0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e)   |
| CaskSubscriptionManager  | [0xfA07af9E5835D720b3798a37f716749252F94D71](https://snowtrace.io/address/0xfA07af9E5835D720b3798a37f716749252F94D71)    |


## Avalanche Supported Stablecoins

| Coin    |                                                        Address                                                         |
|---------|:----------------------------------------------------------------------------------------------------------------------:|
| *USDC.e |  [0xA7D7079b0FEaD91F3e65f86E8915Cb59c1a4C664](https://snowtrace.io/token/0xA7D7079b0FEaD91F3e65f86E8915Cb59c1a4C664)   |
| USDC    |  [0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E](https://snowtrace.io/token/0xB97EF9Ef8734C71904D8002F8b6Bc66Dd9c48a6E)   |
| USDt    |  [0x9702230A8Ea53601f5cD2dc00fDBc13d4dF4A8c7](https://snowtrace.io/token/0x9702230A8Ea53601f5cD2dc00fDBc13d4dF4A8c7)   |
| USDT.e  |  [0xc7198437980c041c805A1EDcbA50c1Ce5db95118](https://snowtrace.io/token/0xc7198437980c041c805A1EDcbA50c1Ce5db95118)   |
| DAI.e   |  [0xd586E7F844cEa2F87f50152665BCbc2C279D8d70](https://snowtrace.io/token/0xd586E7F844cEa2F87f50152665BCbc2C279D8d70)   |

*= Base Asset

## Avalanche Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |    Value    |
|--------------------------|:-----------:|
| Minimum Payment Value    | 1.00 USDC.e |
| Transaction Fee Rate Min |     N/A     |
| Transaction Fee Rate Max |    1.4 %    |
| Minimum Transaction Fee  | 0.50 USDC.e |
| Stake Target Factor      |     N/A     |


### Auto Buys

| Name                    |    Value     |
|-------------------------|:------------:|
| Minimum Buy Amount      | 10.00 USDC.e |
| Transaction Fee         |    0.6 %     |
| Minimum Transaction Fee | 1.00 USDC.e  |
| Minimum Period          |    1 Day     |
| Minimum Slippage        |    0.5 %     |
| Stake Target Factor     |     N/A      |


### Peer to Peer Transfers

| Name                |    Value    |
|---------------------|:-----------:|
| Transaction Fee     | 1.00 USDC.e |
| Stake Target Factor |     N/A     |

# Fantom

## Fantom Contracts

| contract name             |                                                        Address                                                        |
|---------------------------|:---------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0xBCcDbB0806Acc914F6746DE592f924B374190710](https://ftmscan.com/address/0xBCcDbB0806Acc914F6746DE592f924B374190710)  |
| CaskSubscriptions         | [0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360](https://ftmscan.com/address/0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360) |
| CaskSubscriptionPlans     | [0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B](https://ftmscan.com/address/0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B) |
| CaskSubscriptionManager   | [0x17a38EA9257cf899BF9A7F6F507a1445E72F823A](https://ftmscan.com/address/0x17a38EA9257cf899BF9A7F6F507a1445E72F823A) |


## Fantom Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0x04068DA6C83AFCFA0e13ba15A6696662335D5B75](https://ftmscan.com/token/0x04068DA6C83AFCFA0e13ba15A6696662335D5B75) |

*= Base Asset

## Fantom Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

| Name                     |   Value   |
|--------------------------|:---------:|
| Base Asset               |   USDC    | 
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys

| Name                    |   Value   |
|-------------------------|:---------:|
| Minimum Buy Amount      | 5.00 USDC |
| Transaction Fee         |   0.6 %   |
| Minimum Transaction Fee | 0.50 USDC |
| Minimum Period          |   1 Day   |
| Minimum Slippage        |   0.5 %   |
| Stake Target Factor     |    N/A    |


### Peer to Peer Transfers

| Name                |   Value   |
|---------------------|:---------:|
| Transaction Fee     | 0.50 USDC |
| Stake Target Factor |    N/A    |

# Aurora

## Aurora Contracts

| contract name             |                                                         Address                                                         |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://aurorascan.dev/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions         | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://aurorascan.dev/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e) |
| CaskSubscriptionPlans     | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://aurorascan.dev/address/0xD252A4C836C75063867f0193325b328CCe6B7306) |
| CaskSubscriptionManager   | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://aurorascan.dev/address/0x331979A83644574E56035E4b43d3ca68Ce793918) |


## Aurora Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0xB12BFcA5A55806AaF64E99521918A4bf0fC40802](https://aurorascan.dev/token/0xB12BFcA5A55806AaF64E99521918A4bf0fC40802) |

*= Base Asset

## Aurora Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 1.00 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.50 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 1.00 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer to Peer Transfers

| Name                |   Value   |
|---------------------|:---------:|
| Transaction Fee     | 1.00 USDC |
| Stake Target Factor |    N/A    |
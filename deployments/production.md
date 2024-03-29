# Contract Description

| contract name           |                                                                       Description                                                                        |
|-------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|
| CaskVault               |                                                  Cask vault to store the various assets in the protocol                                                  |
| CaskSubscriptions       |      Cask subscriptions contract for subscription flows. Implements ERC-721 for subscriptions to be represented as an optionally transferrable NFT.      |
| CaskSubscriptionPlans   |                                          Cask subscriptions plans contract where the provider profile is held.                                           |
| CaskSubscriptionManager |                                     Processes subscription renewals and holds the subscription protocol parameters.                                      |
| CaskDCA                 |                                    Cask auto-buy (DCA) contract for creating and interacting with the auto-buy flows.                                    |
| CaskDCAManager          |                                   Processes auto-buy (DCA) renewals and holds the auto-buy (DCA) protocol parameters.                                    |
| CaskP2P                 |                                Cask Peer-to-Peer (P2P) contract for creating and interacting with the Peer-to-Peer flows.                                |
| CaskP2PManager          |                               Processes Peer-to-Peer (P2P) renewals and holds the Peer-to-Peer (P2P) protocol parameters.                                |


# Polygon

## Polygon Contracts

| contract name             |                                                          Address                                                          |
|---------------------------|:-------------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://polygonscan.com/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff)  |
| CaskSubscriptions         | [0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0](https://polygonscan.com/address/0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0)  |
| CaskSubscriptionPlans     | [0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e](https://polygonscan.com/address/0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e)  |
| CaskSubscriptionManager   | [0xfA07af9E5835D720b3798a37f716749252F94D71](https://polygonscan.com/address/0xfA07af9E5835D720b3798a37f716749252F94D71)  |
| CaskDCA                   | [0x733Ec5A72c38f2f3c75E98b28DffC1885aB04AF1](https://polygonscan.com/address/0x733Ec5A72c38f2f3c75E98b28DffC1885aB04AF1)  |
| CaskDCAManager            | [0xE07c2e264fb6D4dD8215feD6f3a78d70D1BF4CE2](https://polygonscan.com/address/0xE07c2e264fb6D4dD8215feD6f3a78d70D1BF4CE2)  |
| CaskP2P                   | [0xB80376507Dd5d561AD3A6aB452FE17e782220501](https://polygonscan.com/address/0xB80376507Dd5d561AD3A6aB452FE17e782220501)  |
| CaskP2PManager            | [0xfA7fe9DFFd6fEd7292fdCce2677d88e1b9a9c295](https://polygonscan.com/address/0xfA7fe9DFFd6fEd7292fdCce2677d88e1b9a9c295)  |
| CaskChainlinkTopup        | [0xD621F2C0374d32771d7Cfbec348a63F26f9d7c4F](https://polygonscan.com/address/0xD621F2C0374d32771d7Cfbec348a63F26f9d7c4F)  |
| CaskChainlinkTopupManager | [0x8839A1941A9cB2deCfC05C3191c598Bf2aC5Be0C](https://polygonscan.com/address/0x8839A1941A9cB2deCfC05C3191c598Bf2aC5Be0C)  |


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


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 0.50 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |

### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.10 USDC |
| Minimum Period          |   1 Day   |

### Chainlink Topup

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.9 %    |
| Minimum Transaction Fee | 0.50 USDC  |


# Avalanche

## Avalanche Contracts

| contract name             |                                                        Address                                                        |
|---------------------------|:---------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://snowtrace.io/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions         | [0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0](https://snowtrace.io/address/0x4A6f232552E0fd76787006Bb688bFBCB931cc3d0) |
| CaskSubscriptionPlans     | [0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e](https://snowtrace.io/address/0x78B5882b81AF02ebb0803eAFb4A4bf27fe35470e) |
| CaskSubscriptionManager   | [0xfA07af9E5835D720b3798a37f716749252F94D71](https://snowtrace.io/address/0xfA07af9E5835D720b3798a37f716749252F94D71) |
| CaskDCA                   | [0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8](https://snowtrace.io/address/0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8) |
| CaskDCAManager            | [0x4898D1e6d9761B4215901817FBe9F12750238882](https://snowtrace.io/address/0x4898D1e6d9761B4215901817FBe9F12750238882) |
| CaskP2P                   | [0xe2d24801A9b790f1168cCB7caBdAdC6A071912F3](https://snowtrace.io/address/0xe2d24801A9b790f1168cCB7caBdAdC6A071912F3) |
| CaskP2PManager            | [0xCFC9B780609A80BDF65b4676C3227d2c4c862003](https://snowtrace.io/address/0xCFC9B780609A80BDF65b4676C3227d2c4c862003) |
| CaskChainlinkTopup        | [0xC787791a0d0122b9cCCD2cA9d9FEBcAC3831f0fc](https://snowtrace.io/address/0xC787791a0d0122b9cCCD2cA9d9FEBcAC3831f0fc) |
| CaskChainlinkTopupManager | [0xD621F2C0374d32771d7Cfbec348a63F26f9d7c4F](https://snowtrace.io/address/0xD621F2C0374d32771d7Cfbec348a63F26f9d7c4F) |

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


### Auto Buys (DCA)

| Name                    |    Value     |
|-------------------------|:------------:|
| Minimum Buy Amount      | 20.00 USDC.e |
| Transaction Fee         |    0.6 %     |
| Minimum Transaction Fee | 1.00 USDC.e  |
| Minimum Period          |    1 Day     |
| Minimum Slippage        |    0.5 %     |
| Stake Target Factor     |     N/A      |


### Peer-to-Peer (P2P)

| Name                    |    Value    |
|-------------------------|:-----------:|
| Transaction Fee         | 0.25 USDC.e |
| Minimum Period          |    1 Day    |


### Chainlink Topop

| Name                    |    Value     |
|-------------------------|:------------:|
| Minimum Buy Amount      | 20.00 USDC.e |
| Transaction Fee         |    0.9 %     |
| Minimum Transaction Fee | 1.00 USDC.e  |


# Fantom

## Fantom Contracts

| contract name           |                                                        Address                                                        |
|-------------------------|:---------------------------------------------------------------------------------------------------------------------:|
| CaskVault               | [0xBCcDbB0806Acc914F6746DE592f924B374190710](https://ftmscan.com/address/0xBCcDbB0806Acc914F6746DE592f924B374190710)  |
| CaskSubscriptions       | [0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360](https://ftmscan.com/address/0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360)  |
| CaskSubscriptionPlans   | [0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B](https://ftmscan.com/address/0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B)  |
| CaskSubscriptionManager | [0x17a38EA9257cf899BF9A7F6F507a1445E72F823A](https://ftmscan.com/address/0x17a38EA9257cf899BF9A7F6F507a1445E72F823A)  |
| CaskDCA                 | [0x4C17e4F40262108F06375d727f1353e1D592B1Bf](https://ftmscan.com/address/0x4C17e4F40262108F06375d727f1353e1D592B1Bf)  |
| CaskDCAManager          | [0xfa3ed790FD1fdC5E15c900D929c2F0527a0eC8b6](https://ftmscan.com/address/0xfa3ed790FD1fdC5E15c900D929c2F0527a0eC8b6)  |
| CaskP2P                 | [0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654](https://ftmscan.com/address/0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654)  |
| CaskP2PManager          | [0x8c4E2551542f399Af1576e9c194ea257Dcb7D926](https://ftmscan.com/address/0x8c4E2551542f399Af1576e9c194ea257Dcb7D926)  |

## Fantom Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0x04068DA6C83AFCFA0e13ba15A6696662335D5B75](https://ftmscan.com/token/0x04068DA6C83AFCFA0e13ba15A6696662335D5B75) |

*= Base Asset

## Fantom Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 0.50 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.10 USDC |
| Minimum Period          |   1 Day   |


# Aurora

## Aurora Contracts

| contract name           |                                                         Address                                                         |
|-------------------------|:-----------------------------------------------------------------------------------------------------------------------:|
| CaskVault               | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://aurorascan.dev/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions       | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://aurorascan.dev/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e) |
| CaskSubscriptionPlans   | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://aurorascan.dev/address/0xD252A4C836C75063867f0193325b328CCe6B7306) |
| CaskSubscriptionManager | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://aurorascan.dev/address/0x331979A83644574E56035E4b43d3ca68Ce793918) |
| CaskDCA                 | [0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8](https://aurorascan.dev/address/0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8) |
| CaskDCAManager          | [0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171](https://aurorascan.dev/address/0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171) |
| CaskP2P                 | [0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361](https://aurorascan.dev/address/0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361) |
| CaskP2PManager          | [0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8](https://aurorascan.dev/address/0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8) |

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


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 20.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 1.00 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.25 USDC |
| Minimum Period          |   1 Day   |


# Moonbeam

## Moonbeam Contracts

| contract name           |                                                        Address                                                        |
|-------------------------|:---------------------------------------------------------------------------------------------------------------------:|
| CaskVault               | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://moonscan.io/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff)  |
| CaskSubscriptions       | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://moonscan.io/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e) |
| CaskSubscriptionPlans   | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://moonscan.io/address/0xD252A4C836C75063867f0193325b328CCe6B7306) |
| CaskSubscriptionManager | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://moonscan.io/address/0x331979A83644574E56035E4b43d3ca68Ce793918) |
| CaskDCA                 | [0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8](https://moonscan.io/address/0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8) |
| CaskDCAManager          | [0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171](https://moonscan.io/address/0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171) |
| CaskP2P                 | [0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361](https://moonscan.io/address/0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361) |
| CaskP2PManager          | [0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8](https://moonscan.io/address/0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8) |

## Moonbeam Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0x818ec0A7Fe18Ff94269904fCED6AE3DaE6d6dC0b](https://moonscan.io/token/0x818ec0A7Fe18Ff94269904fCED6AE3DaE6d6dC0b) |

*= Base Asset

## Moonbeam Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 0.50 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.10 USDC |
| Minimum Period          |   1 Day   |


# Gnosis

## Gnosis Contracts

| contract name           |                                                        Address                                                         |
|-------------------------|:----------------------------------------------------------------------------------------------------------------------:|
| CaskVault               | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://gnosisscan.io/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions       | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://gnosisscan.io/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e) |
| CaskSubscriptionPlans   | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://gnosisscan.io/address/0xD252A4C836C75063867f0193325b328CCe6B7306) |
| CaskSubscriptionManager | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://gnosisscan.io/address/0x331979A83644574E56035E4b43d3ca68Ce793918) |
| CaskDCA                 | [0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8](https://gnosisscan.io/address/0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8) |
| CaskDCAManager          | [0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171](https://gnosisscan.io/address/0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171) |
| CaskP2P                 | [0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361](https://gnosisscan.io/address/0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361) |
| CaskP2PManager          | [0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8](https://gnosisscan.io/address/0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8) |

## Gnosis Supported Stablecoins

| Coin  |                                                       Address                                                        |
|-------|:--------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0xDDAfbb505ad214D7b80b1f830fcCc89B60fb7A83](https://gnosisscan.io/token/0xDDAfbb505ad214D7b80b1f830fcCc89B60fb7A83) |
| WXDAI | [0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d](https://gnosisscan.io/token/0xe91D153E0b41518A2Ce8Dd3D7944Fa863463a97d) |

*= Base Asset

## Gnosis Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value   |
|-------------------------|:---------:|
| Minimum Buy Amount      | 5.00 USDC |
| Transaction Fee         |   0.6 %   |
| Minimum Transaction Fee | 0.25 USDC |
| Minimum Period          |   1 Day   |
| Minimum Slippage        |   0.5 %   |
| Stake Target Factor     |    N/A    |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.05 USDC |
| Minimum Period          |   1 Day   |


# Celo

## Celo Contracts

| contract name           |                                                        Address                                                       |
|-------------------------|:--------------------------------------------------------------------------------------------------------------------:|
| CaskVault               | [0xBCcDbB0806Acc914F6746DE592f924B374190710](https://celoscan.io/address/0xBCcDbB0806Acc914F6746DE592f924B374190710) |
| CaskSubscriptions       | [0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360](https://celoscan.io/address/0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360) |
| CaskSubscriptionPlans   | [0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B](https://celoscan.io/address/0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B) |
| CaskSubscriptionManager | [0x17a38EA9257cf899BF9A7F6F507a1445E72F823A](https://celoscan.io/address/0x17a38EA9257cf899BF9A7F6F507a1445E72F823A) |
| CaskDCA                 | [0x4C17e4F40262108F06375d727f1353e1D592B1Bf](https://celoscan.io/address/0x4C17e4F40262108F06375d727f1353e1D592B1Bf) |
| CaskDCAManager          | [0xfa3ed790FD1fdC5E15c900D929c2F0527a0eC8b6](https://celoscan.io/address/0xfa3ed790FD1fdC5E15c900D929c2F0527a0eC8b6) |
| CaskP2P                 | [0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654](https://celoscan.io/address/0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654) |
| CaskP2PManager          | [0x8c4E2551542f399Af1576e9c194ea257Dcb7D926](https://celoscan.io/address/0x8c4E2551542f399Af1576e9c194ea257Dcb7D926) |

## Celo Supported Stablecoins

| Coin           |                                                      Address                                                       |
|----------------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC Wormhole | [0x37f750B7cC259A2f741AF45294f6a16572CF5cAd](https://celoscan.io/token/0x37f750B7cC259A2f741AF45294f6a16572CF5cAd) |
| USDC PoS       | [0x1bfc26cE035c368503fAE319Cc2596716428ca44](https://celoscan.io/token/0x1bfc26cE035c368503fAE319Cc2596716428ca44) |
| cUSD           | [0x765DE816845861e75A25fCA122bb6898B8B1282a](https://celoscan.io/token/0x765DE816845861e75A25fCA122bb6898B8B1282a) |

*= Base Asset

## Celo Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.25 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.05 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value   |
|-------------------------|:---------:|
| Minimum Buy Amount      | 5.00 USDC |
| Transaction Fee         |   0.6 %   |
| Minimum Transaction Fee | 0.25 USDC |
| Minimum Period          |   1 Day   |
| Minimum Slippage        |   0.5 %   |
| Stake Target Factor     |    N/A    |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.05 USDC |
| Minimum Period          |   1 Day   |


# Arbitrum

## Arbitrum Contracts

| contract name             |                                                         Address                                                         |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x20151fF7fDd720b85063D02081aa5B7876aDff7B](https://arbiscan.io/address/0x20151fF7fDd720b85063D02081aa5B7876aDff7B) |
| CaskSubscriptions         | [0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B](https://arbiscan.io/address/0xF76BF31f0b56BD6f72E1aFeB83a51F191ec2291B) |
| CaskSubscriptionPlans     | [0xfA07af9E5835D720b3798a37f716749252F94D71](https://arbiscan.io/address/0xfA07af9E5835D720b3798a37f716749252F94D71) |
| CaskSubscriptionManager   | [0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360](https://arbiscan.io/address/0x7DaF9a1744Df00d0473A9A920B6A4Ea33B665360) |
| CaskDCA                   | [0xf89418E3A57189692ADe9A25792fD986fb99C5Ca](https://arbiscan.io/address/0xf89418E3A57189692ADe9A25792fD986fb99C5Ca) |
| CaskDCAManager            | [0x4C17e4F40262108F06375d727f1353e1D592B1Bf](https://arbiscan.io/address/0x4C17e4F40262108F06375d727f1353e1D592B1Bf) |
| CaskP2P                   | [0x775Df9836945B0E95eD5F6A3269Bf22F6b426e85](https://arbiscan.io/address/0x775Df9836945B0E95eD5F6A3269Bf22F6b426e85) |
| CaskP2PManager            | [0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654](https://arbiscan.io/address/0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654) |
| CaskChainlinkTopup        | [0xe465A32D2826dc5A42FDc75624a18Ee35A25a131](https://arbiscan.io/address/0xe465A32D2826dc5A42FDc75624a18Ee35A25a131) |
| CaskChainlinkTopupManager | [0x7D872c19C5A3839313c76F47CD595Ac843068aCC](https://arbiscan.io/address/0x7D872c19C5A3839313c76F47CD595Ac843068aCC) |

## Arbitrum Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0xFF970A61A04b1cA14834A43f5dE4533eBDDB5CC8](https://arbiscan.io/token/0xFF970A61A04b1cA14834A43f5dE4533eBDDB5CC8) |
| USDT  | [0xFd086bC7CD5C481DCC9C85ebE478A1C0b69FCbb9](https://arbiscan.io/token/0xFd086bC7CD5C481DCC9C85ebE478A1C0b69FCbb9) |
| DAI   | [0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1](https://arbiscan.io/token/0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1) |

*= Base Asset

## Arbitrum Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 0.50 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.10 USDC |
| Minimum Period          |   1 Day   |

### Chainlink Topup

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.9 %    |
| Minimum Transaction Fee | 0.50 USDC  |


# Optimism

## Optimism Contracts

| contract name             |                                                             Address                                                              |
|---------------------------|:--------------------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://optimistic.etherscan.io/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions         | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://optimistic.etherscan.io/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e) |
| CaskSubscriptionPlans     | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://optimistic.etherscan.io/address/0xD252A4C836C75063867f0193325b328CCe6B7306) |
| CaskSubscriptionManager   | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://optimistic.etherscan.io/address/0x331979A83644574E56035E4b43d3ca68Ce793918) |
| CaskDCA                   | [0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8](https://optimistic.etherscan.io/address/0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8) |
| CaskDCAManager            | [0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171](https://optimistic.etherscan.io/address/0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171) |
| CaskP2P                   | [0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361](https://optimistic.etherscan.io/address/0xccB54bF4171bc8C11e78ca40f3a3bd3B721EF361) |
| CaskP2PManager            | [0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8](https://optimistic.etherscan.io/address/0xb8A52a086262E1d6c7494bDCb824f884f41FC5f8) |
| CaskChainlinkTopup        | [0x6deE81A058c48013686520Ac2f5E445dde645062](https://optimistic.etherscan.io/address/0x6deE81A058c48013686520Ac2f5E445dde645062) |
| CaskChainlinkTopupManager | [0xFdbF3Be079AfbD27aE89378839B48Ad7BD18Bbe4](https://optimistic.etherscan.io/address/0xFdbF3Be079AfbD27aE89378839B48Ad7BD18Bbe4) |

## Optimism Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0x7F5c764cBc14f9669B88837ca1490cCa17c31607](https://optimistic.etherscan.io/token/0x7F5c764cBc14f9669B88837ca1490cCa17c31607) |
| USDT  | [0x94b008aA00579c1307B0EF2c499aD98a8ce58e58](https://optimistic.etherscan.io/token/0x94b008aA00579c1307B0EF2c499aD98a8ce58e58) |
| DAI   | [0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1](https://optimistic.etherscan.io/token/0xDA10009cBd5D07dd0CeCc66161FC93D7c9000da1) |

*= Base Asset

## Optimism Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value   |
|--------------------------|:---------:|
| Minimum Payment Value    | 0.50 USDC |
| Transaction Fee Rate Min |    N/A    |
| Transaction Fee Rate Max |   1.4 %   |
| Minimum Transaction Fee  | 0.10 USDC |
| Stake Target Factor      |    N/A    |


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 0.50 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 0.10 USDC |
| Minimum Period          |   1 Day   |

### Chainlink Topup

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 10.00 USDC |
| Transaction Fee         |   0.9 %    |
| Minimum Transaction Fee | 0.50 USDC  |


# BNB Chain

## BNB Chain Contracts

| contract name             |                                                       Address                                                        |
|---------------------------|:--------------------------------------------------------------------------------------------------------------------:|
| CaskVault                 | [0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff](https://bscscan.com/address/0x3b2b4b547dAEEbf3A703288CB43650f0F287b9ff) |
| CaskSubscriptions         | [0xD054F8866fc45c4387d56D2340dCA08d83E14A5e](https://bscscan.com/address/0xD054F8866fc45c4387d56D2340dCA08d83E14A5e)  |
| CaskSubscriptionPlans     | [0xD252A4C836C75063867f0193325b328CCe6B7306](https://bscscan.com/address/0xD252A4C836C75063867f0193325b328CCe6B7306)  |
| CaskSubscriptionManager   | [0x331979A83644574E56035E4b43d3ca68Ce793918](https://bscscan.com/address/0x331979A83644574E56035E4b43d3ca68Ce793918)  |
| CaskDCA                   | [0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8](https://bscscan.com/address/0x96d59127cCD1c0e3749E733Ee04F0DfbD2f808c8)  |
| CaskDCAManager            | [0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171](https://bscscan.com/address/0x83aA6a992Ff3ef3766679Cc90E8C60a04afcC171)  |
| CaskP2P                   | [0x775Df9836945B0E95eD5F6A3269Bf22F6b426e85](https://bscscan.com/address/0x775Df9836945B0E95eD5F6A3269Bf22F6b426e85)  |
| CaskP2PManager            | [0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654](https://bscscan.com/address/0x1A4620123cfD10c73D9Cdd65879c1Fb6312ef654)  |
| CaskChainlinkTopup        | [0x28418B0AB2C00142a865971dcC6a4b1154DaD19E](https://bscscan.com/address/0x28418B0AB2C00142a865971dcC6a4b1154DaD19E)  |
| CaskChainlinkTopupManager | [0x781a5958954a10066feB7B3E94D22D9F8c163e8b](https://bscscan.com/address/0x781a5958954a10066feB7B3E94D22D9F8c163e8b)  |

## BNB Chain Supported Stablecoins

| Coin  |                                                      Address                                                       |
|-------|:------------------------------------------------------------------------------------------------------------------:|
| *USDC | [0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d](https://bscscan.com/token/0x8AC76a51cc950d9822D68b83fE1Ad97B32Cd580d) |
| USDT  | [0x55d398326f99059fF775485246999027B3197955](https://bscscan.com/token/0x55d398326f99059fF775485246999027B3197955) |
| BUSD  | [0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56](https://bscscan.com/token/0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56) |

*= Base Asset

## BNB Chain Protocol Settings and Fees

For details on each fee, see [Protocol Fees](/protocol-fees.md).

### NFT Subscriptions

| Name                     |   Value    |
|--------------------------|:----------:|
| Minimum Payment Value    | 10.00 USDC |
| Transaction Fee Rate Min |    N/A     |
| Transaction Fee Rate Max |   1.4 %    |
| Minimum Transaction Fee  | 2.50 USDC  |
| Stake Target Factor      |    N/A     |


### Auto Buys (DCA)

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 50.00 USDC |
| Transaction Fee         |   0.6 %    |
| Minimum Transaction Fee | 5.00 USDC  |
| Minimum Period          |   1 Day    |
| Minimum Slippage        |   0.5 %    |
| Stake Target Factor     |    N/A     |


### Peer-to-Peer (P2P)

| Name                    |   Value   |
|-------------------------|:---------:|
| Transaction Fee         | 1.50 USDC |
| Minimum Period          |   1 Day   |

### ChainlinkTopup

| Name                    |   Value    |
|-------------------------|:----------:|
| Minimum Buy Amount      | 50.00 USDC |
| Transaction Fee         |   0.9 %    |
| Minimum Transaction Fee | 5.00 USDC  |

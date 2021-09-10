# Relation

## constructor

![image-20210830152749449](https://gitee.com/EYEandEYE/blog_img/raw/master/img/image-20210830152749449.png)

trancheBytecodeHash:

```
0x33353283da9febabe800962de594ae7c9f274743d76e7af5f88afe3e6ea5a94a
```

## function

![image-20210830154407852](https://gitee.com/EYEandEYE/blog_img/raw/master/img/image-20210830154407852.png)



![image-20210830154931980](https://gitee.com/EYEandEYE/blog_img/raw/master/img/image-20210830154931980.png)



# Address & ABI

## Table of Contents
- [InterestTokenFactory](#interesttokenfactory)
- [DateString](#datestring)
- [TrancheFactory](#tranchefactory)
- [WCFX](#wcfx)
- [UserProxy](#userproxy)
- [USDA](#usda)
- [Vault-xUSDA](#Vault-xusda)
- [YVaultAssetProxy](#yvaultassetproxy)
- [BalancerVault](#balancervault)
- [CCPoolFactory](#ccpoolfactory)
## BalancerVault
```
cfxtest:acfgzsywmpxbb7tkf4j8jvuejc3ffhuvjycga9rjhy
```
### ABI
<details>
<summary>ABI</summary>

```json
[
    {
      "inputs": [
        {
          "internalType": "contract IAuthorizer",
          "name": "authorizer",
          "type": "address"
        },
        {
          "internalType": "contract IWETH",
          "name": "weth",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "pauseWindowDuration",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "bufferPeriodDuration",
          "type": "uint256"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "contract IAuthorizer",
          "name": "newAuthorizer",
          "type": "address"
        }
      ],
      "name": "AuthorizerChanged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "token",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "sender",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "address",
          "name": "recipient",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "amount",
          "type": "uint256"
        }
      ],
      "name": "ExternalBalanceTransfer",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "contract IFlashLoanRecipient",
          "name": "recipient",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "token",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "amount",
          "type": "uint256"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "feeAmount",
          "type": "uint256"
        }
      ],
      "name": "FlashLoan",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "user",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "token",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "int256",
          "name": "delta",
          "type": "int256"
        }
      ],
      "name": "InternalBalanceChanged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "internalType": "bool",
          "name": "paused",
          "type": "bool"
        }
      ],
      "name": "PausedStateChanged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "liquidityProvider",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        },
        {
          "indexed": false,
          "internalType": "int256[]",
          "name": "deltas",
          "type": "int256[]"
        },
        {
          "indexed": false,
          "internalType": "uint256[]",
          "name": "protocolFeeAmounts",
          "type": "uint256[]"
        }
      ],
      "name": "PoolBalanceChanged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "assetManager",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "token",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "int256",
          "name": "cashDelta",
          "type": "int256"
        },
        {
          "indexed": false,
          "internalType": "int256",
          "name": "managedDelta",
          "type": "int256"
        }
      ],
      "name": "PoolBalanceManaged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "poolAddress",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "enum IVault.PoolSpecialization",
          "name": "specialization",
          "type": "uint8"
        }
      ],
      "name": "PoolRegistered",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "relayer",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "sender",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "bool",
          "name": "approved",
          "type": "bool"
        }
      ],
      "name": "RelayerApprovalChanged",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "tokenIn",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "contract IERC20",
          "name": "tokenOut",
          "type": "address"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "amountIn",
          "type": "uint256"
        },
        {
          "indexed": false,
          "internalType": "uint256",
          "name": "amountOut",
          "type": "uint256"
        }
      ],
      "name": "Swap",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": false,
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        }
      ],
      "name": "TokensDeregistered",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "indexed": false,
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        },
        {
          "indexed": false,
          "internalType": "address[]",
          "name": "assetManagers",
          "type": "address[]"
        }
      ],
      "name": "TokensRegistered",
      "type": "event"
    },
    {
      "inputs": [],
      "name": "WETH",
      "outputs": [
        {
          "internalType": "contract IWETH",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "enum IVault.SwapKind",
          "name": "kind",
          "type": "uint8"
        },
        {
          "components": [
            {
              "internalType": "bytes32",
              "name": "poolId",
              "type": "bytes32"
            },
            {
              "internalType": "uint256",
              "name": "assetInIndex",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "assetOutIndex",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            },
            {
              "internalType": "bytes",
              "name": "userData",
              "type": "bytes"
            }
          ],
          "internalType": "struct IVault.BatchSwapStep[]",
          "name": "swaps",
          "type": "tuple[]"
        },
        {
          "internalType": "contract IAsset[]",
          "name": "assets",
          "type": "address[]"
        },
        {
          "components": [
            {
              "internalType": "address",
              "name": "sender",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "fromInternalBalance",
              "type": "bool"
            },
            {
              "internalType": "address payable",
              "name": "recipient",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "toInternalBalance",
              "type": "bool"
            }
          ],
          "internalType": "struct IVault.FundManagement",
          "name": "funds",
          "type": "tuple"
        },
        {
          "internalType": "int256[]",
          "name": "limits",
          "type": "int256[]"
        },
        {
          "internalType": "uint256",
          "name": "deadline",
          "type": "uint256"
        }
      ],
      "name": "batchSwap",
      "outputs": [
        {
          "internalType": "int256[]",
          "name": "assetDeltas",
          "type": "int256[]"
        }
      ],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        }
      ],
      "name": "deregisterTokens",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "internalType": "address",
          "name": "sender",
          "type": "address"
        },
        {
          "internalType": "address payable",
          "name": "recipient",
          "type": "address"
        },
        {
          "components": [
            {
              "internalType": "contract IAsset[]",
              "name": "assets",
              "type": "address[]"
            },
            {
              "internalType": "uint256[]",
              "name": "minAmountsOut",
              "type": "uint256[]"
            },
            {
              "internalType": "bytes",
              "name": "userData",
              "type": "bytes"
            },
            {
              "internalType": "bool",
              "name": "toInternalBalance",
              "type": "bool"
            }
          ],
          "internalType": "struct IVault.ExitPoolRequest",
          "name": "request",
          "type": "tuple"
        }
      ],
      "name": "exitPool",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "contract IFlashLoanRecipient",
          "name": "recipient",
          "type": "address"
        },
        {
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        },
        {
          "internalType": "uint256[]",
          "name": "amounts",
          "type": "uint256[]"
        },
        {
          "internalType": "bytes",
          "name": "userData",
          "type": "bytes"
        }
      ],
      "name": "flashLoan",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes4",
          "name": "selector",
          "type": "bytes4"
        }
      ],
      "name": "getActionId",
      "outputs": [
        {
          "internalType": "bytes32",
          "name": "",
          "type": "bytes32"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getAuthorizer",
      "outputs": [
        {
          "internalType": "contract IAuthorizer",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getDomainSeparator",
      "outputs": [
        {
          "internalType": "bytes32",
          "name": "",
          "type": "bytes32"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "user",
          "type": "address"
        },
        {
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        }
      ],
      "name": "getInternalBalance",
      "outputs": [
        {
          "internalType": "uint256[]",
          "name": "balances",
          "type": "uint256[]"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "user",
          "type": "address"
        }
      ],
      "name": "getNextNonce",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getPausedState",
      "outputs": [
        {
          "internalType": "bool",
          "name": "paused",
          "type": "bool"
        },
        {
          "internalType": "uint256",
          "name": "pauseWindowEndTime",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "bufferPeriodEndTime",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        }
      ],
      "name": "getPool",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        },
        {
          "internalType": "enum IVault.PoolSpecialization",
          "name": "",
          "type": "uint8"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "internalType": "contract IERC20",
          "name": "token",
          "type": "address"
        }
      ],
      "name": "getPoolTokenInfo",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "cash",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "managed",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "lastChangeBlock",
          "type": "uint256"
        },
        {
          "internalType": "address",
          "name": "assetManager",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        }
      ],
      "name": "getPoolTokens",
      "outputs": [
        {
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        },
        {
          "internalType": "uint256[]",
          "name": "balances",
          "type": "uint256[]"
        },
        {
          "internalType": "uint256",
          "name": "lastChangeBlock",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getProtocolFeesCollector",
      "outputs": [
        {
          "internalType": "contract ProtocolFeesCollector",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "user",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "relayer",
          "type": "address"
        }
      ],
      "name": "hasApprovedRelayer",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "internalType": "address",
          "name": "sender",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "recipient",
          "type": "address"
        },
        {
          "components": [
            {
              "internalType": "contract IAsset[]",
              "name": "assets",
              "type": "address[]"
            },
            {
              "internalType": "uint256[]",
              "name": "maxAmountsIn",
              "type": "uint256[]"
            },
            {
              "internalType": "bytes",
              "name": "userData",
              "type": "bytes"
            },
            {
              "internalType": "bool",
              "name": "fromInternalBalance",
              "type": "bool"
            }
          ],
          "internalType": "struct IVault.JoinPoolRequest",
          "name": "request",
          "type": "tuple"
        }
      ],
      "name": "joinPool",
      "outputs": [],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "components": [
            {
              "internalType": "enum IVault.PoolBalanceOpKind",
              "name": "kind",
              "type": "uint8"
            },
            {
              "internalType": "bytes32",
              "name": "poolId",
              "type": "bytes32"
            },
            {
              "internalType": "contract IERC20",
              "name": "token",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            }
          ],
          "internalType": "struct IVault.PoolBalanceOp[]",
          "name": "ops",
          "type": "tuple[]"
        }
      ],
      "name": "managePoolBalance",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "components": [
            {
              "internalType": "enum IVault.UserBalanceOpKind",
              "name": "kind",
              "type": "uint8"
            },
            {
              "internalType": "contract IAsset",
              "name": "asset",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            },
            {
              "internalType": "address",
              "name": "sender",
              "type": "address"
            },
            {
              "internalType": "address payable",
              "name": "recipient",
              "type": "address"
            }
          ],
          "internalType": "struct IVault.UserBalanceOp[]",
          "name": "ops",
          "type": "tuple[]"
        }
      ],
      "name": "manageUserBalance",
      "outputs": [],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "enum IVault.SwapKind",
          "name": "kind",
          "type": "uint8"
        },
        {
          "components": [
            {
              "internalType": "bytes32",
              "name": "poolId",
              "type": "bytes32"
            },
            {
              "internalType": "uint256",
              "name": "assetInIndex",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "assetOutIndex",
              "type": "uint256"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            },
            {
              "internalType": "bytes",
              "name": "userData",
              "type": "bytes"
            }
          ],
          "internalType": "struct IVault.BatchSwapStep[]",
          "name": "swaps",
          "type": "tuple[]"
        },
        {
          "internalType": "contract IAsset[]",
          "name": "assets",
          "type": "address[]"
        },
        {
          "components": [
            {
              "internalType": "address",
              "name": "sender",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "fromInternalBalance",
              "type": "bool"
            },
            {
              "internalType": "address payable",
              "name": "recipient",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "toInternalBalance",
              "type": "bool"
            }
          ],
          "internalType": "struct IVault.FundManagement",
          "name": "funds",
          "type": "tuple"
        }
      ],
      "name": "queryBatchSwap",
      "outputs": [
        {
          "internalType": "int256[]",
          "name": "",
          "type": "int256[]"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "enum IVault.PoolSpecialization",
          "name": "specialization",
          "type": "uint8"
        }
      ],
      "name": "registerPool",
      "outputs": [
        {
          "internalType": "bytes32",
          "name": "",
          "type": "bytes32"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bytes32",
          "name": "poolId",
          "type": "bytes32"
        },
        {
          "internalType": "contract IERC20[]",
          "name": "tokens",
          "type": "address[]"
        },
        {
          "internalType": "address[]",
          "name": "assetManagers",
          "type": "address[]"
        }
      ],
      "name": "registerTokens",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "contract IAuthorizer",
          "name": "newAuthorizer",
          "type": "address"
        }
      ],
      "name": "setAuthorizer",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "bool",
          "name": "paused",
          "type": "bool"
        }
      ],
      "name": "setPaused",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "sender",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "relayer",
          "type": "address"
        },
        {
          "internalType": "bool",
          "name": "approved",
          "type": "bool"
        }
      ],
      "name": "setRelayerApproval",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "components": [
            {
              "internalType": "bytes32",
              "name": "poolId",
              "type": "bytes32"
            },
            {
              "internalType": "enum IVault.SwapKind",
              "name": "kind",
              "type": "uint8"
            },
            {
              "internalType": "contract IAsset",
              "name": "assetIn",
              "type": "address"
            },
            {
              "internalType": "contract IAsset",
              "name": "assetOut",
              "type": "address"
            },
            {
              "internalType": "uint256",
              "name": "amount",
              "type": "uint256"
            },
            {
              "internalType": "bytes",
              "name": "userData",
              "type": "bytes"
            }
          ],
          "internalType": "struct IVault.SingleSwap",
          "name": "singleSwap",
          "type": "tuple"
        },
        {
          "components": [
            {
              "internalType": "address",
              "name": "sender",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "fromInternalBalance",
              "type": "bool"
            },
            {
              "internalType": "address payable",
              "name": "recipient",
              "type": "address"
            },
            {
              "internalType": "bool",
              "name": "toInternalBalance",
              "type": "bool"
            }
          ],
          "internalType": "struct IVault.FundManagement",
          "name": "funds",
          "type": "tuple"
        },
        {
          "internalType": "uint256",
          "name": "limit",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "deadline",
          "type": "uint256"
        }
      ],
      "name": "swap",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "amountCalculated",
          "type": "uint256"
        }
      ],
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "stateMutability": "payable",
      "type": "receive"
    }
  ]
```
</details>

## CCPoolFactory
```
cfxtest:ace8s80u8dupkh0b0ctecwct9r5ek068sap9mzgc96
```
### ABI
<details>
<summary>ABI</summary>

```json
[
    {
      "inputs": [
        {
          "internalType": "contract IVault",
          "name": "_vault",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "_governance",
          "type": "address"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "pool",
          "type": "address"
        },
        {
          "indexed": true,
          "internalType": "address",
          "name": "bondToken",
          "type": "address"
        }
      ],
      "name": "CCPoolCreated",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "internalType": "address",
          "name": "pool",
          "type": "address"
        }
      ],
      "name": "PoolCreated",
      "type": "event"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "who",
          "type": "address"
        }
      ],
      "name": "authorize",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "name": "authorized",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "_underlying",
          "type": "address"
        },
        {
          "internalType": "address",
          "name": "_bond",
          "type": "address"
        },
        {
          "internalType": "uint256",
          "name": "_expiration",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_unitSeconds",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "_percentFee",
          "type": "uint256"
        },
        {
          "internalType": "string",
          "name": "_name",
          "type": "string"
        },
        {
          "internalType": "string",
          "name": "_symbol",
          "type": "string"
        }
      ],
      "name": "create",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "who",
          "type": "address"
        }
      ],
      "name": "deauthorize",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "getVault",
      "outputs": [
        {
          "internalType": "contract IVault",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "governance",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "who",
          "type": "address"
        }
      ],
      "name": "isAuthorized",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "pool",
          "type": "address"
        }
      ],
      "name": "isPoolFromFactory",
      "outputs": [
        {
          "internalType": "bool",
          "name": "",
          "type": "bool"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "owner",
      "outputs": [
        {
          "internalType": "address",
          "name": "",
          "type": "address"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "percentFeeGov",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "newGov",
          "type": "address"
        }
      ],
      "name": "setGov",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "uint256",
          "name": "newFee",
          "type": "uint256"
        }
      ],
      "name": "setGovFee",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "internalType": "address",
          "name": "who",
          "type": "address"
        }
      ],
      "name": "setOwner",
      "outputs": [],
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ]
```

</details>
<br>


## InterestTokenFactory
### Testnet
```
cfxtest:accf9dtkkvgh33be9jspt95kvdn2r80veuazn6k0uy
```
### Mainnet
```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "token",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "tranche",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "InterestTokenCreated",
    "type": "event"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_tranche",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "string",
        "name": "_strategySymbol",
        "type": "string"
      },
      {
        "internalType": "uint256",
        "name": "_expiration",
        "type": "uint256"
      },
      {
        "internalType": "uint8",
        "name": "_underlyingDecimals",
        "type": "uint8"
      }
    ],
    "name": "deployInterestToken",
    "outputs": [
      {
        "internalType": "contract InterestToken",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```
</details>
</br>

## DateString
### Testnet
```
cfxtest:aceexxjxcrf9m4fgfpk5rrr23nv2mr5pky72jxzsga
```
### Mainnet
```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
    {
      "inputs": [],
      "name": "OFFSET19700101",
      "outputs": [
        {
          "internalType": "int256",
          "name": "",
          "type": "int256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "SECONDS_PER_DAY",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "SECONDS_PER_HOUR",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    },
    {
      "inputs": [],
      "name": "SECONDS_PER_MINUTE",
      "outputs": [
        {
          "internalType": "uint256",
          "name": "",
          "type": "uint256"
        }
      ],
      "stateMutability": "view",
      "type": "function"
    }
  ]
```
</details>
</br>


## TrancheFactory
### Testnet
```
cfxtest:acgk31mt25khe2mhc6ak60c1u0c49wa5xjjnrrddbv
```

### Mainnet

```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_factory",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "dateLibrary",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "trancheAddress",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "wpAddress",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "uint256",
        "name": "expiration",
        "type": "uint256"
      }
    ],
    "name": "TrancheCreated",
    "type": "event"
  },
  {
    "inputs": [],
    "name": "TRANCHE_CREATION_HASH",
    "outputs": [
      {
        "internalType": "bytes32",
        "name": "",
        "type": "bytes32"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_expiration",
        "type": "uint256"
      },
      {
        "internalType": "address",
        "name": "_wpAddress",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "deployTranche",
    "outputs": [
      {
        "internalType": "contract Tranche",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "getData",
    "outputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      },
      {
        "internalType": "contract IInterestToken",
        "name": "",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  }
]
```
</details>
</br>

### ByteCode
```
7a4b34572d88f842f2ddfa78630d39b85cdfb0b711176aa599bf3192b8bd5395
```
## WCFX
### Testnet
```
cfxtest:acbbuu2y4k736279c40cabjfwcdfp4y4x66eep7ee1 
```

```
0x82184314D27B9e63Bf16AC2005059086566a9A9f
```
### Mainnet
```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Approval",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "dst",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "wad",
        "type": "uint256"
      }
    ],
    "name": "Deposit",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "from",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "to",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Transfer",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "src",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "wad",
        "type": "uint256"
      }
    ],
    "name": "Withdrawal",
    "type": "event"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "allowance",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "approve",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "account",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "balanceOf",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "decimals",
    "outputs": [
      {
        "internalType": "uint8",
        "name": "",
        "type": "uint8"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "subtractedValue",
        "type": "uint256"
      }
    ],
    "name": "decreaseAllowance",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "addedValue",
        "type": "uint256"
      }
    ],
    "name": "increaseAllowance",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "name",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "symbol",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "totalSupply",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "sender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transferFrom",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "deposit",
    "outputs": [],
    "stateMutability": "payable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transfer",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "withdraw",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```
</details>
</br>



## UserProxy
### Testnet

```
cfxtest:acc8k6yz4s9fxu85j397b1k1je1jzferxpgr65ngzx
```

```

```
### Mainnet

```

```
### ABI

<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [
      {
        "internalType": "contract IWETH",
        "name": "_weth",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "__trancheFactory",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "bytes32",
        "name": "__trancheBytecodeHash",
        "type": "bytes32"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "inputs": [],
    "name": "SPONSOR",
    "outputs": [
      {
        "internalType": "contract SponsorWhitelistControl",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "who",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "authorize",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "authorized",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "who",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "deauthorize",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "who",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "isAuthorized",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "isFrozen",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "owner",
    "outputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "who",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "setOwner",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "weth",
    "outputs": [
      {
        "internalType": "contract IWETH",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "stateMutability": "payable",
    "type": "receive"
  },
  {
    "inputs": [
      {
        "internalType": "bool",
        "name": "_newState",
        "type": "bool"
      }
    ],
    "name": "setIsFrozen",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      },
      {
        "internalType": "contract IERC20",
        "name": "_underlying",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_expiration",
        "type": "uint256"
      },
      {
        "internalType": "address",
        "name": "_position",
        "type": "address",
        "networkId": 1
      },
      {
        "components": [
          {
            "internalType": "contract IERC20Permit",
            "name": "tokenContract",
            "type": "address"
          },
          {
            "internalType": "address",
            "name": "who",
            "type": "address"
          },
          {
            "internalType": "uint256",
            "name": "amount",
            "type": "uint256"
          },
          {
            "internalType": "uint256",
            "name": "expiration",
            "type": "uint256"
          },
          {
            "internalType": "bytes32",
            "name": "r",
            "type": "bytes32"
          },
          {
            "internalType": "bytes32",
            "name": "s",
            "type": "bytes32"
          },
          {
            "internalType": "uint8",
            "name": "v",
            "type": "uint8"
          }
        ],
        "internalType": "struct UserProxy.PermitData[]",
        "name": "_permitCallData",
        "type": "tuple[]"
      }
    ],
    "name": "mint",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "payable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_expiration",
        "type": "uint256"
      },
      {
        "internalType": "address",
        "name": "_position",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_amountPT",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "_amountYT",
        "type": "uint256"
      },
      {
        "components": [
          {
            "internalType": "contract IERC20Permit",
            "name": "tokenContract",
            "type": "address"
          },
          {
            "internalType": "address",
            "name": "who",
            "type": "address"
          },
          {
            "internalType": "uint256",
            "name": "amount",
            "type": "uint256"
          },
          {
            "internalType": "uint256",
            "name": "expiration",
            "type": "uint256"
          },
          {
            "internalType": "bytes32",
            "name": "r",
            "type": "bytes32"
          },
          {
            "internalType": "bytes32",
            "name": "s",
            "type": "bytes32"
          },
          {
            "internalType": "uint8",
            "name": "v",
            "type": "uint8"
          }
        ],
        "internalType": "struct UserProxy.PermitData[]",
        "name": "_permitCallData",
        "type": "tuple[]"
      }
    ],
    "name": "withdrawWeth",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "deprecate",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```
</details>
</br>

## USDA
### Testnet
```
cfxtest:acgfgvhxwfeduu07a6pf6u538aj7at2veasb6fxhu0
```

```

```
### Mainnet
```

```
### ABI

<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Approval",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "from",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "to",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Transfer",
    "type": "event"
  },
  {
    "inputs": [],
    "name": "DOMAIN_SEPARATOR",
    "outputs": [
      {
        "internalType": "bytes32",
        "name": "",
        "type": "bytes32"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "PERMIT_TYPEHASH",
    "outputs": [
      {
        "internalType": "bytes32",
        "name": "",
        "type": "bytes32"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "allowance",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "account",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "approve",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "balanceOf",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "decimals",
    "outputs": [
      {
        "internalType": "uint8",
        "name": "",
        "type": "uint8"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "name",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "nonces",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "deadline",
        "type": "uint256"
      },
      {
        "internalType": "uint8",
        "name": "v",
        "type": "uint8"
      },
      {
        "internalType": "bytes32",
        "name": "r",
        "type": "bytes32"
      },
      {
        "internalType": "bytes32",
        "name": "s",
        "type": "bytes32"
      }
    ],
    "name": "permit",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "symbol",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transfer",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transferFrom",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "faucet",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```

</details>
</br>

## Vault-xUSDA

### Testnet
```
cfxtest:acfj6eu4w68d0732kn77afa9agrj9uzpmpeyvsue5g
```
### Mainnet

```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_underlyTokenAddr",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Approval",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "from",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "to",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Transfer",
    "type": "event"
  },
  {
    "inputs": [],
    "name": "addr",
    "outputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "allowance",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "approve",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "account",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "balanceOf",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "decimals",
    "outputs": [
      {
        "internalType": "uint8",
        "name": "",
        "type": "uint8"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "subtractedValue",
        "type": "uint256"
      }
    ],
    "name": "decreaseAllowance",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "addedValue",
        "type": "uint256"
      }
    ],
    "name": "increaseAllowance",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "name",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "symbol",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "token",
    "outputs": [
      {
        "internalType": "contract ERC20",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "totalSupply",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transfer",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "sender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transferFrom",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_underlyTokenAddr",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "setAddr",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      },
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "deposit",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_shares",
        "type": "uint256"
      },
      {
        "internalType": "address",
        "name": "_destination",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_minUnderlying",
        "type": "uint256"
      }
    ],
    "name": "_withdraw",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "pricePerShare",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "totalAssets",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "apiVersion",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  }
]
```
</details>
</br>

## YVaultAssetProxy
### Testnet
```
cfxtest:acfkmkfse864y16cn9261y5j2785d75rmeed68hskd
```

```

```
### Mainnet
```

```
### ABI
<details>
<summary>ABI</summary>

```json
[
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "vault_",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "contract IERC20",
        "name": "_token",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "string",
        "name": "_name",
        "type": "string"
      },
      {
        "internalType": "string",
        "name": "_symbol",
        "type": "string"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "constructor",
    "name": "constructor"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Approval",
    "type": "event"
  },
  {
    "anonymous": false,
    "inputs": [
      {
        "indexed": true,
        "internalType": "address",
        "name": "from",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": true,
        "internalType": "address",
        "name": "to",
        "type": "address",
        "networkId": 1
      },
      {
        "indexed": false,
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      }
    ],
    "name": "Transfer",
    "type": "event"
  },
  {
    "inputs": [],
    "name": "DOMAIN_SEPARATOR",
    "outputs": [
      {
        "internalType": "bytes32",
        "name": "",
        "type": "bytes32"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "PERMIT_TYPEHASH",
    "outputs": [
      {
        "internalType": "bytes32",
        "name": "",
        "type": "bytes32"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "allowance",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "balanceOf",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_who",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "balanceOfUnderlying",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "decimals",
    "outputs": [
      {
        "internalType": "uint8",
        "name": "",
        "type": "uint8"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_destination",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      }
    ],
    "name": "deposit",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_shares",
        "type": "uint256"
      }
    ],
    "name": "getSharesToUnderlying",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "name",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "nonces",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "owner",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "value",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "deadline",
        "type": "uint256"
      },
      {
        "internalType": "uint8",
        "name": "v",
        "type": "uint8"
      },
      {
        "internalType": "bytes32",
        "name": "r",
        "type": "bytes32"
      },
      {
        "internalType": "bytes32",
        "name": "s",
        "type": "bytes32"
      }
    ],
    "name": "permit",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_destination",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "prefundedDeposit",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "name": "reserveBalances",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "reserveShares",
    "outputs": [
      {
        "internalType": "uint128",
        "name": "",
        "type": "uint128"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "reserveSupply",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "reserveUnderlying",
    "outputs": [
      {
        "internalType": "uint128",
        "name": "",
        "type": "uint128"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "symbol",
    "outputs": [
      {
        "internalType": "string",
        "name": "",
        "type": "string"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "token",
    "outputs": [
      {
        "internalType": "contract IERC20",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transfer",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "spender",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "address",
        "name": "recipient",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "transferFrom",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "vault",
    "outputs": [
      {
        "internalType": "contract IYearnVault",
        "name": "",
        "type": "address",
        "networkId": 1
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "vaultDecimals",
    "outputs": [
      {
        "internalType": "uint8",
        "name": "",
        "type": "uint8"
      }
    ],
    "stateMutability": "view",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_destination",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_shares",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "_minUnderlying",
        "type": "uint256"
      }
    ],
    "name": "withdraw",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "_destination",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "_minUnderlying",
        "type": "uint256"
      }
    ],
    "name": "withdrawUnderlying",
    "outputs": [
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      },
      {
        "internalType": "uint256",
        "name": "",
        "type": "uint256"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      }
    ],
    "name": "reserveDeposit",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "uint256",
        "name": "_amount",
        "type": "uint256"
      }
    ],
    "name": "reserveWithdraw",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [
      {
        "internalType": "address",
        "name": "account",
        "type": "address",
        "networkId": 1
      },
      {
        "internalType": "uint256",
        "name": "amount",
        "type": "uint256"
      }
    ],
    "name": "approve",
    "outputs": [
      {
        "internalType": "bool",
        "name": "",
        "type": "bool"
      }
    ],
    "stateMutability": "nonpayable",
    "type": "function"
  },
  {
    "inputs": [],
    "name": "approve",
    "outputs": [],
    "stateMutability": "nonpayable",
    "type": "function"
  }
]
```
</details>
</br>
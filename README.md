# Address & ABI

## Table of Contents
- [InterestTokenFactory](#interesttokenfactory)
- [DateString](#datestring)
- [TrancheFactory](#tranchefactory)
- [WCFX](#wcfx)
- [UserProxy](#userproxy)
- [GLD](#gld)
- [Yault-xGLD](#yault-xgld)
- [YVaultAssetProxy](#yvaultassetproxy)

## InterestTokenFactory
### Testnet
```
cfxtest:accf9dtkkvgh33be9jspt95kvdn2r80veuazn6k0uy
```
```

```
### Mainnet
```

```
### ABI
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

## DateString
### Testnet
```
cfxtest:aceexxjxcrf9m4fgfpk5rrr23nv2mr5pky72jxzsga
```

```

```
### Mainnet
```

```
### ABI
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

## TrancheFactory
### Testnet
```
cfxtest:acfab1dxxam2xxtf9ku1gh5vjkhah8uvjp8khytsgw 
```

```

```
### Mainnet
```

```
### ABI
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

## UserProxy
### Testnet
```
cfxtest:acfr36z84u1t9km1j3c3ppb0tcas88r5se30k3e8bx
```

```

```
### Mainnet
```

```
### ABI
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
## GLD
### Testnet
```
cfxtest:acak2d1reg7h33r1pahp1rf1unu3w196s2ggejty5s
```

```
0x809c0EED21Ba7Ce5B7600ecBb4b782e1995fFc76
```
### Mainnet
```

```
### ABI
```json

```

## Yault-xGLD
### Testnet
```
cfxtest:acfphmx1j2byjpzntp80wwrd3v4earj16ac5dgrkn6
```

```
0x8aC3Aa7746034432Ab7b3D6949A3cC74403517E0
```
### Mainnet
```

```
### ABI
```json

```

## YVaultAssetProxy
### Testnet
```
cfxtest:acak2d1reg7h33r1pahp1rf1unu3w196s2ggejty5s
```

```
0x809c0EED21Ba7Ce5B7600ecBb4b782e1995fFc76
```
### Mainnet
```

```
### ABI
```json


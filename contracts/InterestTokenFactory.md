# InterestTokenFactory
## Testnet
```
cfxtest:accf9dtkkvgh33be9jspt95kvdn2r80veuazn6k0uy
```
## ABI
```json
[
	{
		"anonymous": false,
		"inputs": [
			{
				"indexed": true,
				"internalType": "address",
				"name": "token",
				"type": "address"
			},
			{
				"indexed": true,
				"internalType": "address",
				"name": "tranche",
				"type": "address"
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
				"type": "address"
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
				"type": "address"
			}
		],
		"stateMutability": "nonpayable",
		"type": "function"
	}
]
```

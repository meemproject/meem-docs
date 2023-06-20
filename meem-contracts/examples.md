# Examples

Let's take a look at some scenarios and how you can set up the contract to support them.

### Varied minting cost

* A holder of token XYZ should be able to mint at a price of 0.1 MATIC
* Anyone else can mint at a price of 2 MATIC

```typescript
import { ethers } from 'ethers'
import { initProxy, zeroAddress Chain, Permission, defaultBaseProperties } from '@meemproject/meem-contracts'

export async function variedMinting(options: {
	contractAddress: string
	signer: ethers.Wallet
}) {
	const { contractAddress, signer } = options

	const tx = await initProxy({
		signer,
		proxyContractAddress: contractAddress,
		chain: Chain.Polygon,
		name: 'Test Meem',
		symbol: 'TME',
		contractURI:
			'{"name": "Test","description": "testing","image": "","external_link": ""}',
		baseProperties: {
			...defaultBaseProperties,
			mintPermissions: [
				// Holders of WETH can mint for a price of 0.1 MATIC
				{
					permission: Permission.Holders,
					addresses: ['0x7ceb23fd6bc0add59e62ac25578270cff1b9f619'],
					costWei: ethers.utils.parseEther('0.1'),
					numTokens: 1,
					lockedBy: zeroAddress
				},
				// Everyone else can mint for 2 MATIC
				{
					permission: Permission.Anyone,
					addresses: [],
					costWei: ethers.utils.parseEther('2'),
					numTokens: 0,
					lockedBy: zeroAddress
				}
			],
			// Split proceeds between 2 wallets. 25% and 75%
			splits: [
				{
					toAddress: '0x...',
					amount: 2500,
					lockedBy: zeroAddress
				},
				{
					toAddress: '0x...',
					amount: 7500,
					lockedBy: zeroAddress
				}
			]
		}
	})

	console.log(`Initialized contract with tx: ${tx.hash}`)
}
```


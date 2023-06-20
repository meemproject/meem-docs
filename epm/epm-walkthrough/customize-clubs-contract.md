# Customize Clubs Contract

This walkthrough will go through the process of manually customizing a Clubs contract. For the sake of this example let's say that you want to code special requirements to mint that the Meem Contracts do not support out of the box.

We'll create a contract that implements the `requireCanMint` function and then use EPM to use that function for our Club.

### Step 1: Create a Club

Head over to [https://clubs.link](https://clubs.link) and create a club

### Step 2: Get the club address

In your club settings, grab the contract address

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.35.24 PM.png" alt=""><figcaption></figcaption></figure>

### Step 3: Write a Contract with Special Permissions

For this (silly) example, we'll only allow minting for odd-numbered timestamps

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.13;

struct RequireCanMintParams {
	address minter;
	address to;
	bytes32[] proof;
}

contract MyCustomFacet {
	function requireCanMint(RequireCanMintParams memory params) public payable {
		if (block.timestamp % 2 == 0) {
			revert('Minting only allowed for odd-numbered timestamps');
		}
	}
}
```

### Step 4: Upload Contract to EPM

Head over to [https://epm.wtf/create](https://epm.wtf/create) and upload your contract. See [Creating a Contract](creating-a-contract.md) for more info.

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.48.48 PM.png" alt=""><figcaption></figcaption></figure>

### Step 5: Deploy Contract

Next you'll need to actually deploy the contract you just created. On the contract details page. Find the contract you uploaded and deploy it from [https://epm.wtf/contracts](https://epm.wtf/contracts)

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.51.31 PM.png" alt=""><figcaption></figcaption></figure>

### Step 6: Attach Function

Take the club address you just copied and drop it into EPM at:

[https://epm.wtf/manage](https://epm.wtf/manage)

The page should show you all the current facets and associated functions. You can toggle which contract handles what function(s).

#### Turn off existing requireCanMint function

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.53.04 PM.png" alt=""><figcaption></figcaption></figure>

#### Add the contract we just created

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.53.20 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.53.30 PM.png" alt=""><figcaption></figcaption></figure>

### Step 7: Save the Changes

When you save, you're triggering a Diamond Cut which will tell our Diamond Proxy Contract that it should use our new contract for the `requireCanMint` function

<figure><img src="../../.gitbook/assets/Screen Shot 2022-09-02 at 3.57.53 PM.png" alt=""><figcaption></figcaption></figure>

### Congrats!

You've now customized your clubs contract with custom minting requirements. What other use cases can you dream up?

# Ethereum Package Manager

Deploying and managing contracts is not a super-straightforward endeavor. You need to be comfortable with solidity tooling like hardhat and using a command line. In many cases customization of a smart contract is not necessary. You may just need to deploy a standard Openzeppelin ERC-20 contract but don’t want to go deep into getting an environment set up for compiling and deployment.

[Ethereum Package Manager (EPM)](https://epm.wtf) is a tool to deploy and manage smart contracts. At it’s most basic, you can search and deploy contracts using a web UI and a familiar wallet like Metamask. If you need a custom contract, you can also upload your own (bytecode and abi).

{% hint style="info" %}
Try it yourself at [https://epm.wtf](https://epm.wtf)
{% endhint %}

However, EPM offers much more functionality than just simply deploying smart contracts. It also lets you manage proxy contracts and compose contracts together using a web UI. Additionally you can download Typescript types and code snippets to quickly start interacting with contracts.

<figure><img src="../.gitbook/assets/Screen Shot 2022-09-07 at 9.53.42 AM.png" alt=""><figcaption></figcaption></figure>

EIP-1167 is the most widely used proxy pattern today. A proxy contract uses the [fallback mechanism in solidity](https://blog.openzeppelin.com/proxy-patterns/) so you can upgrade the logic layer of your contract while keeping the data intact. In this pattern you have 2 contracts:

1. The proxy contract. This is where data is stored. It acts as purely a pass-through to the logic contract. It also allows switching the address of the logic contract which is what allows for upgradability.
2. The logic contract. This contains all the business logic of the contract.

The [EIP-2535 proxy standard](https://eips.ethereum.org/EIPS/eip-2535) is the next evolution of the proxy pattern. Instead of a single logic contract, you can have as many logic contracts (called “facets” in the diamond pattern) as you need. This has many benefits:

* Workaround for the 24kb contract size limit
* Reusable and composable logic contracts

If you’re not familiar with the EIP-2535 proxy pattern [check out this great introduction](https://eip2535diamonds.substack.com/p/introduction-to-the-diamond-standard) and [find more resources](eip-2535-further-reading.md).

# Meem Smart Contracts

The core Meem team develops open-source smart contract standards with the goal of supporting a wide variety of use cases.

### TL;DR No-code Smart Contract Management

Deploy and manage your smart contracts using a web interface developed by the core Meem team. You can upgrade to new versions of the Meem Protocol or change your smart contract settings.

Everything we build is on top of our [open-source packages](https://github.com/meemproject/meem-packages) which includes smart contracts, react components, typescript types, and various other utilities.

## Under the Hood

In order to facilitate future upgrades to Meem contracts, we use [EIP-2535 Diamond proxies](https://eips.ethereum.org/EIPS/eip-2535). This pattern splits logic into multiple smart contracts which are called via the main proxy contract.

This has many benefits including:

* Unlimited extensibility. Since logic can be split into multiple facets and a diamond can have an unlimited number of facets there is no limit on functionality that can be added ([no 24kb contract size limit](https://dev.to/mudgen/ethereum-s-maximum-contract-size-limit-is-solved-with-the-diamond-standard-2189))
* Multiple proxy contracts can use the same facet contracts.

![Multiple contracts using facet versions](<../.gitbook/assets/image (2).png>)

### Source Code

{% embed url="https://github.com/meemproject/meem-packages/tree/dev/packages/meem-contracts" %}

## Ongoing Development

The Meem Team is continuously iterating on the smart contracts that are used to define relationships between things and people. [Check out the corresponding version docs](meem-contract-versions/). And remember you can always [upgrade your contract](../epm/epm-walkthrough/upgrade-a-contract.md) to take advantage of the latest features!

Continue reading the following sections to get an overview of some of the features available by using Meem Contracts.

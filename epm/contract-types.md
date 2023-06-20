# Contract Types

For the purposes of EPM there are 3 contract types to be aware of:

### 1. Diamond Proxy

These are contracts that implement the Diamond Proxy standard. They take advantage of [the fallback function in solidity](https://docs.soliditylang.org/en/v0.8.13/contracts.html#fallback-function) to route incoming requests to the proper Facet. The implementation maintained by the Meem Team [can be found on github](https://github.com/meemproject/meem-packages/blob/dev/packages/meem-contracts/contracts/proxies/MeemDiamond.sol).

### 2. Diamond Facet

A facet contains part of the business logic for the contract. Functions from a facet are attached to a Proxy.

### 3. Any Other Smart Contract ("regular" contract)

EPM also supports uploading and deploying of non-diamond smart contracts.

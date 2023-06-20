# Creating a Contract

### Find your contract ABI and bytecode

When you compile your solidity code, look in the `artifacts/` directory. You'll should find a json file `MyContract.sol/MyContract.json` that contains both the `abi` and `bytecode`.

![](<../../.gitbook/assets/Screen Shot 2022-06-28 at 1.50.16 PM.png>)

{% hint style="danger" %}
**Make sure you use `bytecode` and NOT `deployedByteCode` from the json file.**

`deployedByteCode` [does not contain constructor code](https://medium.com/coinmonks/the-difference-between-bytecode-and-deployed-bytecode-64594db723df)
{% endhint %}

### Upload the contract

{% embed url="https://epm.wtf/create" %}
Upload a contract to epm.wtf
{% endembed %}

Once uploaded, your contract will be available for deployment.

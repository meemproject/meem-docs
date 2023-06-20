# Composable Contracts

Before reading further, you should be familiar with the concepts of [EIP-2535](https://eip2535diamonds.substack.com/p/introduction-to-the-diamond-standard) which introduces the Diamond Pattern for smart contracts.

EPM empowers you add facets, remove facets, and toggle facet functions on/off. This opens up some interesting possibilities to compose contracts together. For example, you could start with a simple, audited ERC-721 (facet) contract that has already been deployed. Then with EPM you could override only the function you need. Maybe you only need to change the `tokenURI()` method. Instead of deploying a full ERC-721 contract with that one minor change. This is the approach we’ve taken with another Meem product, [Clubs](https://clubs.link). Here’s an example of the facets we use for Clubs: [view clubs contract on EPM](https://epm.wtf/manage?address=0xcf169E3D03e46df50f609Ac3b49B66f453E5b6fc\&chainId=137).

![](<../.gitbook/assets/Screen Shot 2022-08-17 at 9.53.49 AM.png>)

In the screenshot you can see that some functions are toggled off on the ERC-721 facet. The `handleSaleDistribution(...)` method is disabled on the base contract and then implemented on the Splits facet. In the above scenario, there is logic in the ERC-721 contract that will call `handleSaleDistribution(...)` when a token is minted. The base contract does nothing - it just returns whatever `msg.value` was sent back to the sender. The Splits facet however implements custom logic that allows for distribution based on splits (royalties) to multiple parties.

Similarly, `requireCanMint(...)` is turned off at the base contract and implemented on a custom Permissions facet that adheres to the rules we’ve created for Clubs. But maybe you want to have all the functionality we use for Clubs but have your own custom rules for minting. You can simply implement that one method in a facet contract but continue to use all the other already deployed facet contracts for the rest of the logic.

This composability is incredibly powerful. You can override exactly the methods you need and re-use logic contracts with any proxy contract. A nice side benefit of composing contracts like this is that you only need to deploy logic contracts that haven’t already been deployed which saves on contract deployment costs.

{% content-ref url="epm-walkthrough/customize-clubs-contract.md" %}
[customize-clubs-contract.md](epm-walkthrough/customize-clubs-contract.md)
{% endcontent-ref %}

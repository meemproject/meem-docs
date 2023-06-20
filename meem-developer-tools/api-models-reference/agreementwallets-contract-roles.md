# AgreementWallets (Contract Roles)

`MeemContractWallets` keeps track of roles that have been assigned **at the contract level.** Currently with Meem Contracts there are 3 roles that can be granted that each have special abilities.

#### ADMIN\_ROLE

The admin role allows for changing contract information like name or symbol as well as defining permissions, splits, and more.

#### MINTER\_ROLE

The minter role bypasses minting permission checks.

#### UPGRADER\_ROLE

The upgrader role allows a wallet to perform contract upgrades.

{% hint style="info" %}
The contract owner can always upgrade regardless of assigned roles
{% endhint %}

<table><thead><tr><th width="164">Name</th><th width="273">Description</th><th width="179">Data Type</th><th>On-chain?</th></tr></thead><tbody><tr><td><code>id</code></td><td>Id of the token</td><td><code>UUID</code></td><td>N</td></tr><tr><td><code>role</code></td><td>The role the user has on the contract</td><td><code>string (hex)</code></td><td>Y</td></tr><tr><td><code>mintedAt</code></td><td>When the token was minted</td><td><code>DateTime</code></td><td>Y</td></tr><tr><td><code>createdAt</code></td><td>When the contract was created</td><td><code>DateTime</code></td><td>Y</td></tr><tr><td><code>updatedAt</code></td><td>When the item was last updated</td><td><code>DateTime</code></td><td>N</td></tr><tr><td><code>Wallet</code></td><td>The <a href="wallets.md">Wallet</a> that has been granted a role</td><td><a href="wallets.md">Wallet</a></td><td>Y</td></tr><tr><td><code>MeemContract</code></td><td>The corresponding <a href="agreements.md">MeemContract</a></td><td><a href="agreements.md">MeemContract</a></td><td>Y</td></tr><tr><td><code>WalletId</code></td><td>The wallet id of the user</td><td><code>UUID</code></td><td>N</td></tr><tr><td><code>MeemContractId</code></td><td>The corresponding contract where the wallet holds the role</td><td><code>UUID</code></td><td>N</td></tr></tbody></table>

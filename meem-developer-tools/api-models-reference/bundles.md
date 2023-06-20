# Bundles

`Bundles` are a collection of contracts that can be "cut" into an EIP-2535 Diamond Proxy Contract.

<table><thead><tr><th width="164">Name</th><th width="273">Description</th><th width="179">Data Type</th></tr></thead><tbody><tr><td><code>id</code></td><td>Id of the bundle</td><td><code>UUID</code></td></tr><tr><td><code>name</code></td><td>Name of the bundle</td><td><code>string</code></td></tr><tr><td><code>description</code></td><td>A description of the bundle</td><td><code>string</code></td></tr><tr><td><code>CreatorId</code></td><td>The id of the Wallet that created the bundle. This is the only user who can update the bundle in the future.</td><td>UUID</td></tr><tr><td><code>abi</code></td><td>The combined abi of all the contracts in the bundle</td><td><code>string</code></td></tr><tr><td><code>types</code></td><td>The typechain types generated from the combined abi</td><td><code>string</code></td></tr><tr><td><code>createdAt</code></td><td>When the contract was created</td><td><code>DateTime</code></td></tr><tr><td><code>updatedAt</code></td><td>When the item was last updated</td><td><code>DateTime</code></td></tr></tbody></table>


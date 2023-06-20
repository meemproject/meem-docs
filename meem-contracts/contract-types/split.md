# Split

A split defines a wallet address that should receive a portion / royalty when a Meem is minted or re-sold

| Parameter Name | Type    | Description                                                                  |
| -------------- | ------- | ---------------------------------------------------------------------------- |
| `toAddress`    | address | The address that should receive a percentage of the sale.                    |
| `amount`       | uint256 | The amount that should be received _in basis points_. (5% == 500)            |
| `lockedBy`     | address | Locks this split so it can't be changed. If not locked, use the zero-address |

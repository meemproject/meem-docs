# Permission

### Permission Enum

A permission defines who and under what circumstances. The `Permission` enum:

| Enum Option | Description                                             |
| ----------- | ------------------------------------------------------- |
| `Anyone`    | Permission applies to anyone.                           |
| `Addresses` | Permission applies to any address in this array         |
| `Holders`   | Permission applies to holders of the token(s) specified |

### Permission Item

Permission items are used to define who can mint, remix, copy, and read Meems. Each permission item specifies:

| Parameter Name       | Type            | Description                                                                            |
| -------------------- | --------------- | -------------------------------------------------------------------------------------- |
| `permission`         | Permission enum | The permission type                                                                    |
| `addresses`          | address\[]      | Array of addresses. Only applicable to `Permission.Addresses` and `Permission.Holders` |
| `numTokens`          | uint256         | The number of tokens required (if applicable) for this permission.                     |
| `costWei`            | uint256         | The cost in wei to perform this action.                                                |
| `mintStartTimestamp` | uint256         | Unix timestamp (seconds) When the mint starts (0 for open).                            |
| `mintEndTimestamp`   | uint256         | <p>Unix timestamp (seconds) </p><p>When the mint ends (0 for open)</p>                 |


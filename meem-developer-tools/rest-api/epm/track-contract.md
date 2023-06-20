# Track Contract

Will track this contract so that it will show up in My Contracts in EPM.

**Endpoint:** `/api/1.0/contractInstances`

**Authenticated Request:** Yes

**Method:** `POST`

**Request Body Parameters**

| Parameter Name | Data Type (required) | Description                                                               |
| -------------- | -------------------- | ------------------------------------------------------------------------- |
| **address**    | `string (Y)`         | The contract address                                                      |
| **chainId**    | `number (Y)`         | The [EVM chain id](https://chainlist.org/) where the contract is deployed |

**Response Body**

| Parameter Name | Data Type | Description       |
| -------------- | --------- | ----------------- |
| **status**     | `string`  | Will be "success" |


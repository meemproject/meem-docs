# Update Bundle

**Endpoint:** `/api/1.0/bundles/:bundleId`

**Authenticated Request:** Yes

**Method:** `PUT`

**Request Body Parameters**

| Parameter Name  | Data Type (required)                               | Description                                                                                                    |
| --------------- | -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **name**        | `string (Y)`                                       | The name of the bundle                                                                                         |
| **description** | `string (Y)`                                       | A description of the bundle                                                                                    |
| **contracts**   | `{ id: string functionSelectors: string[] }[] (Y)` | Defines which contracts are part of the bundle **AND** which function selectors are turned on for the contract |

**Response Body**

| Parameter Name | Data Type  | Description                                   |
| -------------- | ---------- | --------------------------------------------- |
| **types**      | `string`   | The generated typescript types for the bundle |
| **abi**        | JSON Array | The combined ABI for the bundle               |


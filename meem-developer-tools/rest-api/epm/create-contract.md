# Create Contract

**Endpoint:** `/api/1.0/contracts`

**Authenticated Request:** Yes

**Method:** `POST`

**Request Body Parameters**

| Parameter Name   | Data Type (required) | Description                                                                                            |
| ---------------- | -------------------- | ------------------------------------------------------------------------------------------------------ |
| **name**         | `string (Y)`         | The name of the contract                                                                               |
| **description**  | `string (Y)`         | A description of the contract                                                                          |
| **contractType** | `string (Y)`         | <p>One of:<br>- <code>regular</code><br>- <code>diamondProxy</code><br>- <code>diamondFacet</code></p> |
| **abi**          | JSON Array `(Y)`     | The ABI of the contract                                                                                |
| **bytecode**     | `string (Y)`         | The contract bytecode                                                                                  |

**Response Body**

| Parameter Name | Data Type | Description                                                           |
| -------------- | --------- | --------------------------------------------------------------------- |
| **status**     | `string`  | Will be "success"                                                     |
| **contractId** | `UUID`    | The contract id which can be used to make requests to other endpoints |


# Generate Types

Generate Typescript types

**Endpoint:** `/api/1.0/generateTypes`

**Authenticated Request:** Yes

**Method:** `POST`

**Request Body Parameters**

{% hint style="info" %}
**Either `abi` OR `bundleId` is required**
{% endhint %}

| Parameter Name | Data Type (Required) | Description                                                               |
| -------------- | -------------------- | ------------------------------------------------------------------------- |
| **abi**        | `JSON Array (N)`     | The ABI definition to generate types from                                 |
| **bundleId**   | `UUID (N)`           | The EPM bundle id (Bundle.id) to generate types from                      |
| **name**       | `string (N)`         | The name to use for the generated contract types. Default is "MyContract" |

**Response Body**

| Parameter Name | Data Type | Description       |
| -------------- | --------- | ----------------- |
| **status**     | `string`  | Will be "success" |




---
description: 'TODO: Description of Meem SDK'
---

# Javascript/Typescript SDK

### Login

```typescript
import { MeemSDK } from '@meemproject/sdk'

const result = await sdk.id.login({
    message: "Welcome to Meem!", // The message that will appear in the user's wallet to sign
    signer: {...}, // The signer <JsonRpcSigner>
    chainId: 5, // The chainId
    uri: window.location.href; // The URI where the login is taking place
})

/**
result: {
    signature: string;
    authSig: {
        sig: string;
        derivedVia: string;
        signedMessage: string;
        address: string;
    };
    jwt: string;
    messageToSign: string;
}
*/
```

###

### Create an Agreement

```typescript
TODO
```



### Bulk Mint Agreement Tokens

```typescript
TODO
```



### Reinitialize an Agreement

```typescript
TODO
```



### Create an Agreement Role

```typescript
TODO
```



### Bulk Mint Agreement Role Tokens

```typescript
TODO
```



### Reinitialize an Agreement Role

```typescript
TODO
```

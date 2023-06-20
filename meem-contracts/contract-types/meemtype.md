# MeemType

The Meem type falls into 4 categories which are defined by an `enum`:

| Enum Option | Description                                                                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Original`  | An original. Not derived from or inspired by any other Meem                                                                                           |
| `Copy`      | A copy or "edition" references a parent token and uses the same metadata as the original.                                                             |
| `Remix`     | A derivative of an original or remix. Has it's own metadata.                                                                                          |
| `Wrapped`   | A special type that can only be minted by users with the `MINTER_ROLE`. These tokens represent ownership of a token on a different contract or chain. |

```typescript
import { MeemType } from '@meemproject/meem-contracts'

console.log(MeemType.Original)
```

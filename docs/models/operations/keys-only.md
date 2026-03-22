# KeysOnly

When 'true', omits the data payload and returns only keys + timestamps. Useful for state overview without transferring large payloads.

## Example Usage

```typescript
import { KeysOnly } from "bereach/models/operations";

let value: KeysOnly = "false";
```

## Values

```typescript
"true" | "false"
```
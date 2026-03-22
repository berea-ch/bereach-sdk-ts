# ListAgentStatesRequest

## Example Usage

```typescript
import { ListAgentStatesRequest } from "bereach/models/operations";

let value: ListAgentStatesRequest = {};
```

## Fields

| Field                                                                                                                                  | Type                                                                                                                                   | Required                                                                                                                               | Description                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `keysOnly`                                                                                                                             | [operations.KeysOnly](../../models/operations/keys-only.md)                                                                            | :heavy_minus_sign:                                                                                                                     | When 'true', omits the data payload and returns only keys + timestamps. Useful for state overview without transferring large payloads. |
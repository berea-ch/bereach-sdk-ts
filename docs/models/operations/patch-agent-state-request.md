# PatchAgentStateRequest

## Example Usage

```typescript
import { PatchAgentStateRequest } from "bereach/models/operations";

let value: PatchAgentStateRequest = {
  key: "<key>",
  body: {
    data: {
      "key": "<value>",
      "key1": "<value>",
      "key2": "<value>",
    },
  },
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `key`                                                                                              | *string*                                                                                           | :heavy_check_mark:                                                                                 | State key                                                                                          |
| `body`                                                                                             | [operations.PatchAgentStateRequestBody](../../models/operations/patch-agent-state-request-body.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
# SetAgentStateRequest

## Example Usage

```typescript
import { SetAgentStateRequest } from "bereach/models/operations";

let value: SetAgentStateRequest = {
  key: "<key>",
  body: {
    data: "<value>",
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `key`                                                                                          | *string*                                                                                       | :heavy_check_mark:                                                                             | State key                                                                                      |
| `body`                                                                                         | [operations.SetAgentStateRequestBody](../../models/operations/set-agent-state-request-body.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
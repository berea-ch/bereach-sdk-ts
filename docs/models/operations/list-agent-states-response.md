# ListAgentStatesResponse

All state entries

## Example Usage

```typescript
import { ListAgentStatesResponse } from "bereach/models/operations";

let value: ListAgentStatesResponse = {
  success: true,
  states: [],
  creditsUsed: 222501,
  retryAfter: 187764,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `states`                                                                           | [operations.State](../../models/operations/state.md)[]                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |
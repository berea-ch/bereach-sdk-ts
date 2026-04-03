# PullTaskResponse

Task pulled (or null)

## Example Usage

```typescript
import { PullTaskResponse } from "bereach/models/operations";

let value: PullTaskResponse = {
  task: {
    id: "<id>",
    type: "<value>",
    campaignId: null,
    message: "<value>",
    model: "XTS",
    thinking: "<value>",
    timeoutSeconds: 65313,
    sessionKey: "<value>",
    payload: null,
  },
  cancelTaskId: "<id>",
  pollIntervalMs: 676177,
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `task`                                                               | [operations.PullTaskTask](../../models/operations/pull-task-task.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `cancelTaskId`                                                       | *string*                                                             | :heavy_check_mark:                                                   | ID of a recently cancelled task the connector should abort           |
| `pollIntervalMs`                                                     | *number*                                                             | :heavy_check_mark:                                                   | Suggested poll interval in ms (5000 when busy, 30000 when idle)      |
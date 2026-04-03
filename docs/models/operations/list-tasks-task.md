# ListTasksTask

## Example Usage

```typescript
import { ListTasksTask } from "bereach/models/operations";

let value: ListTasksTask = {
  id: "<id>",
  type: "<value>",
  campaignId: "<id>",
  status: "running",
  priority: 750834,
  model: null,
  result: "<value>",
  error: "<value>",
  connectorId: "<id>",
  workflowRunId: "<id>",
  createdAt: "1722140098349",
  dispatchedAt: "<value>",
  completedAt: "<value>",
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `id`                                                            | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `type`                                                          | *string*                                                        | :heavy_check_mark:                                              | Task type (e.g. lead-gen-qualify, outreach-batch, lm-comments)  |
| `campaignId`                                                    | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `status`                                                        | [operations.TaskStatus](../../models/operations/task-status.md) | :heavy_check_mark:                                              | N/A                                                             |
| `priority`                                                      | *number*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `model`                                                         | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `result`                                                        | *any*                                                           | :heavy_check_mark:                                              | Structured task result (after completion)                       |
| `error`                                                         | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `connectorId`                                                   | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `workflowRunId`                                                 | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `createdAt`                                                     | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `dispatchedAt`                                                  | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
| `completedAt`                                                   | *string*                                                        | :heavy_check_mark:                                              | N/A                                                             |
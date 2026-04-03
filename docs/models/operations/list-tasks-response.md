# ListTasksResponse

Task list

## Example Usage

```typescript
import { ListTasksResponse } from "bereach/models/operations";

let value: ListTasksResponse = {
  tasks: [
    {
      id: "<id>",
      type: "<value>",
      campaignId: "<id>",
      status: "failed",
      priority: 747767,
      model: "Impala",
      result: "<value>",
      error: "<value>",
      connectorId: "<id>",
      workflowRunId: "<id>",
      createdAt: "1724488524726",
      dispatchedAt: "<value>",
      completedAt: "<value>",
    },
  ],
  total: 71781,
  limit: 46815,
  offset: 368745,
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `tasks`                                                                  | [operations.ListTasksTask](../../models/operations/list-tasks-task.md)[] | :heavy_check_mark:                                                       | N/A                                                                      |
| `total`                                                                  | *number*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `limit`                                                                  | *number*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
| `offset`                                                                 | *number*                                                                 | :heavy_check_mark:                                                       | N/A                                                                      |
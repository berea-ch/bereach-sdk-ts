# ListTasksRequest

## Example Usage

```typescript
import { ListTasksRequest } from "bereach/models/operations";

let value: ListTasksRequest = {};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `status`                                                                                         | [operations.ListTasksQueryParamStatus](../../models/operations/list-tasks-query-param-status.md) | :heavy_minus_sign:                                                                               | Filter by task status                                                                            |
| `type`                                                                                           | *string*                                                                                         | :heavy_minus_sign:                                                                               | Filter by task type (e.g. outreach-batch)                                                        |
| `campaignId`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | Filter by campaign ID                                                                            |
| `limit`                                                                                          | *number*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `offset`                                                                                         | *number*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
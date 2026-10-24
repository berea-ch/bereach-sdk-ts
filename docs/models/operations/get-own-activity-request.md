# GetOwnActivityRequest

## Example Usage

```typescript
import { GetOwnActivityRequest } from "bereach/models/operations";

let value: GetOwnActivityRequest = {};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `tabType`                                                                       | [operations.QueryParamTabType](../../models/operations/query-param-tab-type.md) | :heavy_minus_sign:                                                              | Type of activity to fetch                                                       |
| `count`                                                                         | *number*                                                                        | :heavy_minus_sign:                                                              | Number of items per page (max 50)                                               |
| `start`                                                                         | *number*                                                                        | :heavy_minus_sign:                                                              | Pagination offset                                                               |
| `paginationToken`                                                               | *string*                                                                        | :heavy_minus_sign:                                                              | Pagination token from previous response                                         |
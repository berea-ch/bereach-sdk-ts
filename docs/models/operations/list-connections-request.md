# ListConnectionsRequest

## Example Usage

```typescript
import { ListConnectionsRequest } from "bereach/models/operations";

let value: ListConnectionsRequest = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `start`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Pagination offset                                           |
| `count`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Results per page (max 40)                                   |
| `sortType`                                                  | [operations.SortType](../../models/operations/sort-type.md) | :heavy_minus_sign:                                          | Sort order (default RECENTLY_ADDED)                         |
| `keywords`                                                  | *string*                                                    | :heavy_minus_sign:                                          | Filter connections by name                                  |
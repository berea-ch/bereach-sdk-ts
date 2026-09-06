# SearchEmployeesResponse

People at the company

## Example Usage

```typescript
import { SearchEmployeesResponse } from "bereach/models/operations";

let value: SearchEmployeesResponse = {
  success: true,
  company: "Nikolaus Group",
  items: [
    {
      type: "PEOPLE",
      name: "<value>",
      profileUrl: null,
      headline: "<value>",
      location: "<value>",
      profilePicture: "<value>",
      networkDistance: "DISTANCE_1",
      currentPositions: [],
      profileUrn: "<value>",
      publicIdentifier: null,
    },
  ],
  paging: {
    start: 329787,
    count: 734982,
    total: 160955,
  },
  hasMore: true,
  creditsUsed: 235103,
  retryAfter: 682986,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `company`                                                                                                                                 | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Resolved company key used for the search (slug or name as passed after parse).                                                            |
| `items`                                                                                                                                   | [operations.SearchEmployeesItem](../../models/operations/search-employees-item.md)[]                                                      | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `paging`                                                                                                                                  | [operations.SearchEmployeesPaging](../../models/operations/search-employees-paging.md)                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `hasMore`                                                                                                                                 | *boolean*                                                                                                                                 | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `warnings`                                                                                                                                | [operations.SearchEmployeesWarning](../../models/operations/search-employees-warning.md)[]                                                | :heavy_minus_sign:                                                                                                                        | Caveats about this result set. Absent or empty means the search ran exactly as asked.                                                     |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.SearchEmployeesMeta](../../models/operations/search-employees-meta.md)                                                        | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |
# ListLinkedInCompanyPagesResponse

List of managed company pages

## Example Usage

```typescript
import { ListLinkedInCompanyPagesResponse } from "bereach/models/operations";

let value: ListLinkedInCompanyPagesResponse = {
  success: true,
  pages: [
    {
      id: "<id>",
      universalName: "<value>",
      name: "<value>",
      url: "https://pale-championship.name",
      logoUrl: "https://jaunty-meadow.org/",
      followerCount: 2682.14,
      industry: null,
      employeeCount: 505.49,
      adminRole: "<value>",
    },
  ],
  total: 85006,
  creditsUsed: 74529,
  retryAfter: 999218,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `pages`                                                                              | [operations.Page](../../models/operations/page.md)[]                                 | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `total`                                                                              | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |
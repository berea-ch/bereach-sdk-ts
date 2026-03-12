# UpsertContactsResponse

Contacts created or updated

## Example Usage

```typescript
import { UpsertContactsResponse } from "bereach/models/operations";

let value: UpsertContactsResponse = {
  success: true,
  results: {
    created: 20897,
    updated: 534346,
    skipped: 566490,
    errors: [
      "<value 1>",
    ],
  },
  contacts: [],
  creditsUsed: 848749,
  retryAfter: 326324,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `success`                                                                          | *true*                                                                             | :heavy_check_mark:                                                                 | N/A                                                                                |
| `results`                                                                          | [operations.Results](../../models/operations/results.md)                           | :heavy_check_mark:                                                                 | N/A                                                                                |
| `contacts`                                                                         | [operations.ContactResponse](../../models/operations/contact-response.md)[]        | :heavy_check_mark:                                                                 | Full contact objects with IDs for immediate use                                    |
| `creditsUsed`                                                                      | *number*                                                                           | :heavy_check_mark:                                                                 | Credits consumed by this call (always 0 for contacts queries).                     |
| `retryAfter`                                                                       | *number*                                                                           | :heavy_check_mark:                                                                 | Seconds to wait before next call of the same type (always 0 for contacts queries). |
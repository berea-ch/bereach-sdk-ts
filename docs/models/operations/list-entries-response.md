# ListEntriesResponse

Context entries

## Example Usage

```typescript
import { ListEntriesResponse } from "bereach/models/operations";

let value: ListEntriesResponse = {
  success: true,
  entries: [],
  creditsUsed: 506601,
  retryAfter: 896596,
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `success`                                                                      | *true*                                                                         | :heavy_check_mark:                                                             | N/A                                                                            |
| `entries`                                                                      | [operations.ListEntriesEntry](../../models/operations/list-entries-entry.md)[] | :heavy_check_mark:                                                             | N/A                                                                            |
| `creditsUsed`                                                                  | *number*                                                                       | :heavy_check_mark:                                                             | Credits consumed (always 0 for workspace operations).                          |
| `retryAfter`                                                                   | *number*                                                                       | :heavy_check_mark:                                                             | Seconds to wait (always 0 for workspace operations).                           |
# GetFeedRequest

## Example Usage

```typescript
import { GetFeedRequest } from "bereach/models/operations";

let value: GetFeedRequest = {};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `count`                                                                       | *number*                                                                      | :heavy_minus_sign:                                                            | Number of feed items to return (1-50, default 20)                             |
| `sortOrder`                                                                   | [operations.SortOrder](../../models/operations/sort-order.md)                 | :heavy_minus_sign:                                                            | Sort order: RELEVANCE (default, algorithmic) or REV_CHRON (most recent first) |
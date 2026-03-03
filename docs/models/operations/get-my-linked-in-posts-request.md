# GetMyLinkedInPostsRequest

## Example Usage

```typescript
import { GetMyLinkedInPostsRequest } from "bereach/models/operations";

let value: GetMyLinkedInPostsRequest = {};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `count`                                                           | *number*                                                          | :heavy_minus_sign:                                                | Number of posts to fetch (default 20, max 100).                   |
| `start`                                                           | *number*                                                          | :heavy_minus_sign:                                                | Pagination offset (default 0).                                    |
| `paginationToken`                                                 | *string*                                                          | :heavy_minus_sign:                                                | Pagination token from a previous response to fetch the next page. |
# CollectLinkedInCommentRepliesRequest

## Example Usage

```typescript
import { CollectLinkedInCommentRepliesRequest } from "bereach/models/operations";

let value: CollectLinkedInCommentRepliesRequest = {
  commentUrn: "<value>",
};
```

## Fields

| Field                                                                                                                                       | Type                                                                                                                                        | Required                                                                                                                                    | Description                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `commentUrn`                                                                                                                                | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Comment URN returned by the comments endpoint (e.g., 'urn:li:comment:(activity:123456,789)').                                               |
| `start`                                                                                                                                     | *number*                                                                                                                                    | :heavy_minus_sign:                                                                                                                          | Pagination offset (default 0).                                                                                                              |
| `count`                                                                                                                                     | *number*                                                                                                                                    | :heavy_minus_sign:                                                                                                                          | Number of replies to fetch per page (0-100, default 100). Use count=0 for a free total-only check (0 credits, no rate-limit slot consumed). |
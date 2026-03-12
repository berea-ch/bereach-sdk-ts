# CollectLinkedInHashtagPostsRequest

## Example Usage

```typescript
import { CollectLinkedInHashtagPostsRequest } from "bereach/models/operations";

let value: CollectLinkedInHashtagPostsRequest = {
  hashtag: "<value>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `hashtag`                                 | *string*                                  | :heavy_check_mark:                        | Hashtag to collect posts from (without #) |
| `start`                                   | *number*                                  | :heavy_minus_sign:                        | Pagination offset                         |
| `count`                                   | *number*                                  | :heavy_minus_sign:                        | Number of posts                           |
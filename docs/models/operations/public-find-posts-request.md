# PublicFindPostsRequest

## Example Usage

```typescript
import { PublicFindPostsRequest } from "bereach/models/operations";

let value: PublicFindPostsRequest = {
  query: "<value>",
};
```

## Fields

| Field                                                                                                                                                     | Type                                                                                                                                                      | Required                                                                                                                                                  | Description                                                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `query`                                                                                                                                                   | *string*                                                                                                                                                  | :heavy_check_mark:                                                                                                                                        | Topic keyword or hashtag to search posts for.                                                                                                             |
| `limit`                                                                                                                                                   | *number*                                                                                                                                                  | :heavy_minus_sign:                                                                                                                                        | Target number of posts.                                                                                                                                   |
| `more`                                                                                                                                                    | *boolean*                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                        | Continue past what an earlier call on this same ask already returned, instead of returning it again. What counts as already returned is kept server side. |
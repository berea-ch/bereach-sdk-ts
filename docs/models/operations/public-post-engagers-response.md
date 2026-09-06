# PublicPostEngagersResponse

Post data with commenters

## Example Usage

```typescript
import { PublicPostEngagersResponse } from "bereach/models/operations";

let value: PublicPostEngagersResponse = {
  source: "public",
  hydrated: true,
  savedCommenters: 694925,
  post: {
    "key": "<value>",
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `source`                                                                                      | [operations.PublicPostEngagersSource](../../models/operations/public-post-engagers-source.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `hydrated`                                                                                    | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `savedCommenters`                                                                             | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `post`                                                                                        | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | Post text, author, date, counts, and commenters.                                              |
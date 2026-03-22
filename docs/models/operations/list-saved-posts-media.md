# ListSavedPostsMedia

## Example Usage

```typescript
import { ListSavedPostsMedia } from "bereach/models/operations";

let value: ListSavedPostsMedia = {
  type: "video",
  urls: [
    "<value 1>",
    "<value 2>",
  ],
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `type`                                                                            | [operations.ListSavedPostsType](../../models/operations/list-saved-posts-type.md) | :heavy_check_mark:                                                                | Type of media attached to the post.                                               |
| `urls`                                                                            | *string*[]                                                                        | :heavy_check_mark:                                                                | Media URLs (image URLs for carousels, video streaming URL, article link, etc.).   |
| `title`                                                                           | *string*                                                                          | :heavy_minus_sign:                                                                | Title of the article or document, when available.                                 |
| `thumbnailUrl`                                                                    | *string*                                                                          | :heavy_minus_sign:                                                                | Thumbnail URL for videos, articles, or document covers.                           |
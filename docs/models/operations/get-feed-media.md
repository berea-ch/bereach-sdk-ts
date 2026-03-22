# GetFeedMedia

Media attached to the post (image, video, document, or article). Absent when the post is text-only.

## Example Usage

```typescript
import { GetFeedMedia } from "bereach/models/operations";

let value: GetFeedMedia = {
  type: "image",
  urls: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `type`                                                                          | [operations.GetFeedMediaType](../../models/operations/get-feed-media-type.md)   | :heavy_check_mark:                                                              | Type of media attached to the post.                                             |
| `urls`                                                                          | *string*[]                                                                      | :heavy_check_mark:                                                              | Media URLs (image URLs for carousels, video streaming URL, article link, etc.). |
| `title`                                                                         | *string*                                                                        | :heavy_minus_sign:                                                              | Title of the article or document, when available.                               |
| `thumbnailUrl`                                                                  | *string*                                                                        | :heavy_minus_sign:                                                              | Thumbnail URL for videos, articles, or document covers.                         |
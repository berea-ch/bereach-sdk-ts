# SearchLinkedInMedia

Media attached to the post (image, video, document, or article). Absent when the post is text-only.

## Example Usage

```typescript
import { SearchLinkedInMedia } from "bereach/models/operations";

let value: SearchLinkedInMedia = {
  type: "document",
  urls: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `type`                                                                                       | [operations.SearchLinkedInMediaType](../../models/operations/search-linked-in-media-type.md) | :heavy_check_mark:                                                                           | Type of media attached to the post.                                                          |
| `urls`                                                                                       | *string*[]                                                                                   | :heavy_check_mark:                                                                           | Media URLs (image URLs for carousels, video streaming URL, article link, etc.).              |
| `title`                                                                                      | *string*                                                                                     | :heavy_minus_sign:                                                                           | Title of the article or document, when available.                                            |
| `thumbnailUrl`                                                                               | *string*                                                                                     | :heavy_minus_sign:                                                                           | Thumbnail URL for videos, articles, or document covers.                                      |
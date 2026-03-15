# SearchLinkedInByUrlMedia

Media attached to the post (image, video, document, or article). Absent when the post is text-only.

## Example Usage

```typescript
import { SearchLinkedInByUrlMedia } from "bereach/models/operations";

let value: SearchLinkedInByUrlMedia = {
  type: "video",
  urls: [],
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                   | [operations.SearchLinkedInByUrlMediaType](../../models/operations/search-linked-in-by-url-media-type.md) | :heavy_check_mark:                                                                                       | Type of media attached to the post.                                                                      |
| `urls`                                                                                                   | *string*[]                                                                                               | :heavy_check_mark:                                                                                       | Media URLs (image URLs for carousels, video streaming URL, article link, etc.).                          |
| `title`                                                                                                  | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Title of the article or document, when available.                                                        |
| `thumbnailUrl`                                                                                           | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Thumbnail URL for videos, articles, or document covers.                                                  |
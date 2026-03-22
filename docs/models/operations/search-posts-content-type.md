# SearchPostsContentType

Filter by media type. Only return posts that contain the specified media. 'images' = photo posts, 'videos' = video posts, 'documents' = carousel/PDF posts.

## Example Usage

```typescript
import { SearchPostsContentType } from "bereach/models/operations";

let value: SearchPostsContentType = "images";
```

## Values

```typescript
"images" | "videos" | "documents"
```
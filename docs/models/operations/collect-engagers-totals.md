# CollectEngagersTotals

The post's own engagement badges, summed across the posts read. A sum, so it can never answer how many came from one post: `perPost` answers that. Absent while `count` is above 0 means the badge could not be read, never that nobody engaged. Both zero or absent WITH count 0 is the only shape that means no visible engagement on this page.

## Example Usage

```typescript
import { CollectEngagersTotals } from "bereach/models/operations";

let value: CollectEngagersTotals = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `likes`            | *number*           | :heavy_minus_sign: | N/A                |
| `comments`         | *number*           | :heavy_minus_sign: | N/A                |
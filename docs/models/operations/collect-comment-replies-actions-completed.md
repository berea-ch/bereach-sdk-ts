# CollectCommentRepliesActionsCompleted

Per-profile action completion status within the campaign. Only present when campaignSlug is provided in the request.

## Example Usage

```typescript
import { CollectCommentRepliesActionsCompleted } from "bereach/models/operations";

let value: CollectCommentRepliesActionsCompleted = {
  message: false,
  reply: false,
  like: true,
  visit: false,
  connect: true,
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `message`          | *boolean*          | :heavy_check_mark: | N/A                |
| `reply`            | *boolean*          | :heavy_check_mark: | N/A                |
| `like`             | *boolean*          | :heavy_check_mark: | N/A                |
| `visit`            | *boolean*          | :heavy_check_mark: | N/A                |
| `connect`          | *boolean*          | :heavy_check_mark: | N/A                |
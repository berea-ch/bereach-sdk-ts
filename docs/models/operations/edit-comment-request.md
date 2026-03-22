# EditCommentRequest

## Example Usage

```typescript
import { EditCommentRequest } from "bereach/models/operations";

let value: EditCommentRequest = {
  text: "<value>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `fsdCommentUrn`                                                                    | *string*                                                                           | :heavy_minus_sign:                                                                 | urn:li:fsd_comment:(COMMENT_ID,urn:li:ugcPost:POST_ID) - from comment API response |
| `commentUrn`                                                                       | *string*                                                                           | :heavy_minus_sign:                                                                 | Legacy comment URN format                                                          |
| `text`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | New comment text                                                                   |
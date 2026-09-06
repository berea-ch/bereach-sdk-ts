# Deleted

## Example Usage

```typescript
import { Deleted } from "bereach/models/operations";

let value: Deleted = {
  type: "ugcPost",
  parentId: "<id>",
  commentId: "<id>",
  alreadyGone: true,
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `type`                                                                         | [operations.DeleteCommentType](../../models/operations/delete-comment-type.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `parentId`                                                                     | *string*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `commentId`                                                                    | *string*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `alreadyGone`                                                                  | *boolean*                                                                      | :heavy_check_mark:                                                             | N/A                                                                            |
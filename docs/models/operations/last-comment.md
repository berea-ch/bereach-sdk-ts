# LastComment

## Example Usage

```typescript
import { LastComment } from "bereach/models/operations";

let value: LastComment = {
  type: "reaction",
  activityUrn: "<value>",
  text: "<value>",
  reactionType: "<value>",
  targetPostUrn: "<value>",
  targetPostText: "<value>",
  targetPostAuthor: "<value>",
  timestamp: 1061.1,
  actorName: "<value>",
  actorUrn: "<value>",
};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                  | [operations.LastCommentType](../../models/operations/last-comment-type.md)                              | :heavy_check_mark:                                                                                      | Activity type: 'comment' for posts the user commented on                                                |
| `activityUrn`                                                                                           | *string*                                                                                                | :heavy_check_mark:                                                                                      | URN of the feed update (post) the user engaged with                                                     |
| `text`                                                                                                  | *string*                                                                                                | :heavy_check_mark:                                                                                      | The user's comment text (null when not available from the API — this is a LinkedIn limitation)          |
| `reactionType`                                                                                          | *string*                                                                                                | :heavy_check_mark:                                                                                      | Reaction type (e.g. 'LIKE', 'CELEBRATE'). Only set for reaction-type activities                         |
| `targetPostUrn`                                                                                         | *string*                                                                                                | :heavy_check_mark:                                                                                      | URN of the post the user commented on (e.g. 'urn:li:activity:1234567890')                               |
| `targetPostText`                                                                                        | *string*                                                                                                | :heavy_check_mark:                                                                                      | First ~200 chars of the post the user commented on. Use this to understand what topics they engage with |
| `targetPostAuthor`                                                                                      | *string*                                                                                                | :heavy_check_mark:                                                                                      | Name of the post author (the person whose post was commented on)                                        |
| `timestamp`                                                                                             | *number*                                                                                                | :heavy_check_mark:                                                                                      | Unix timestamp in milliseconds when the activity occurred                                               |
| `actorName`                                                                                             | *string*                                                                                                | :heavy_check_mark:                                                                                      | Name of the post author (same as targetPostAuthor when available)                                       |
| `actorUrn`                                                                                              | *string*                                                                                                | :heavy_check_mark:                                                                                      | Profile URN of the post author                                                                          |
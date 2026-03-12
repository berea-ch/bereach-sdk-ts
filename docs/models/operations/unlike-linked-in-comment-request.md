# UnlikeLinkedInCommentRequest

## Example Usage

```typescript
import { UnlikeLinkedInCommentRequest } from "bereach/models/operations";

let value: UnlikeLinkedInCommentRequest = {
  commentUrn: "<value>",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `commentUrn`                                                               | *string*                                                                   | :heavy_check_mark:                                                         | Full comment URN to unlike (e.g. urn:li:comment:(urn:li:activity:123,456)) |
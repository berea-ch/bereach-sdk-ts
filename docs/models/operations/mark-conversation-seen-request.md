# MarkConversationSeenRequest

## Example Usage

```typescript
import { MarkConversationSeenRequest } from "bereach/models/operations";

let value: MarkConversationSeenRequest = {
  conversationUrn: "<value>",
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                              | *string*                                                                                       | :heavy_check_mark:                                                                             | Full conversation URN (e.g. 'urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)') |
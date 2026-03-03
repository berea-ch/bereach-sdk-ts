# GetConversationMessagesMessage

## Example Usage

```typescript
import { GetConversationMessagesMessage } from "bereach/models/operations";

let value: GetConversationMessagesMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 121889,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "Kieran",
    lastName: "Jenkins",
    profileUrl: "https://speedy-schnitzel.com",
    headline: "<value>",
    profilePicture: "<value>",
  },
  attachments: [],
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `messageUrn`                                                                                                      | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `text`                                                                                                            | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `deliveredAt`                                                                                                     | *number*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `senderProfileUrn`                                                                                                | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `sender`                                                                                                          | [operations.GetConversationMessagesSender](../../models/operations/get-conversation-messages-sender.md)           | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `attachments`                                                                                                     | [operations.GetConversationMessagesAttachment](../../models/operations/get-conversation-messages-attachment.md)[] | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
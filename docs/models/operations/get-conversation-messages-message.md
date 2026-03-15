# GetConversationMessagesMessage

## Example Usage

```typescript
import { GetConversationMessagesMessage } from "bereach/models/operations";

let value: GetConversationMessagesMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 573952,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "Paxton",
    lastName: "Zboncak",
    profileUrl: "https://altruistic-metabolite.net",
    headline: "<value>",
    profilePicture: "<value>",
    publicIdentifier: "<value>",
    profileUrn: "<value>",
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
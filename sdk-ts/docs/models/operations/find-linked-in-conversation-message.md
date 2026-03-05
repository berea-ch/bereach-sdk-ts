# FindLinkedInConversationMessage

## Example Usage

```typescript
import { FindLinkedInConversationMessage } from "bereach/models/operations";

let value: FindLinkedInConversationMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 299315,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "George",
    lastName: "Hane",
    profileUrl: "https://sophisticated-formula.info",
    headline: "<value>",
    profilePicture: "<value>",
  },
  attachments: [
    {
      type: "file",
    },
  ],
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `messageUrn`                                                                                                         | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `text`                                                                                                               | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `deliveredAt`                                                                                                        | *number*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `senderProfileUrn`                                                                                                   | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `sender`                                                                                                             | [operations.FindLinkedInConversationSender](../../models/operations/find-linked-in-conversation-sender.md)           | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `attachments`                                                                                                        | [operations.FindLinkedInConversationAttachment](../../models/operations/find-linked-in-conversation-attachment.md)[] | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
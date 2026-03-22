# FindConversationMessage

## Example Usage

```typescript
import { FindConversationMessage } from "bereach/models/operations";

let value: FindConversationMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 56601,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "Kendrick",
    lastName: "Sawayn-Boyle",
    profileUrl: "https://front-newsprint.org",
    headline: "<value>",
    profilePicture: "<value>",
    publicIdentifier: null,
    profileUrn: "<value>",
  },
  attachments: [
    {
      type: "image",
    },
  ],
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `messageUrn`                                                                                       | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `text`                                                                                             | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `deliveredAt`                                                                                      | *number*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `senderProfileUrn`                                                                                 | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `sender`                                                                                           | [operations.FindConversationSender](../../models/operations/find-conversation-sender.md)           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `attachments`                                                                                      | [operations.FindConversationAttachment](../../models/operations/find-conversation-attachment.md)[] | :heavy_check_mark:                                                                                 | N/A                                                                                                |
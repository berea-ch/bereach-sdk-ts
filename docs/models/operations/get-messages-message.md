# GetMessagesMessage

## Example Usage

```typescript
import { GetMessagesMessage } from "bereach/models/operations";

let value: GetMessagesMessage = {
  messageUrn: "<value>",
  text: "<value>",
  deliveredAt: 990581,
  senderProfileUrn: "<value>",
  sender: {
    firstName: "Samson",
    lastName: "Trantow",
    profileUrl: "https://everlasting-farm.com",
    headline: "<value>",
    profilePicture: "<value>",
    publicIdentifier: "<value>",
    profileUrn: "<value>",
  },
  attachments: [
    {
      type: "file",
    },
  ],
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `messageUrn`                                                                             | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `text`                                                                                   | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `deliveredAt`                                                                            | *number*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `senderProfileUrn`                                                                       | *string*                                                                                 | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `sender`                                                                                 | [operations.GetMessagesSender](../../models/operations/get-messages-sender.md)           | :heavy_check_mark:                                                                       | N/A                                                                                      |
| `attachments`                                                                            | [operations.GetMessagesAttachment](../../models/operations/get-messages-attachment.md)[] | :heavy_check_mark:                                                                       | N/A                                                                                      |
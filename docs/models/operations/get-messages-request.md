# GetMessagesRequest

## Example Usage

```typescript
import { GetMessagesRequest } from "bereach/models/operations";

let value: GetMessagesRequest = {
  conversationUrn: "<value>",
};
```

## Fields

| Field                                                                                                                         | Type                                                                                                                          | Required                                                                                                                      | Description                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                                                             | *string*                                                                                                                      | :heavy_check_mark:                                                                                                            | Full conversation URN as returned by /chats/linkedin (e.g. 'urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)') |
| `deliveredAt`                                                                                                                 | *number*                                                                                                                      | :heavy_minus_sign:                                                                                                            | Timestamp (ms) of the oldest message from previous page — pass this to load older messages                                    |
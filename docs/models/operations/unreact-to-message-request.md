# UnreactToMessageRequest

## Example Usage

```typescript
import { UnreactToMessageRequest } from "bereach/models/operations";

let value: UnreactToMessageRequest = {
  messageUrn: "<value>",
  emoji: "<value>",
  conversationUrn: "<value>",
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `messageUrn`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | Full message URN (e.g. 'urn:li:msg_message:(urn:li:fsd_profile:ACoAAXXX,2-MTcw...)') |
| `emoji`                                                                              | *string*                                                                             | :heavy_check_mark:                                                                   | Emoji character to react with (e.g. '👍', '❤️', '😂')                                |
| `conversationUrn`                                                                    | *string*                                                                             | :heavy_check_mark:                                                                   | Conversation URN (required for the old messaging API fallback)                       |
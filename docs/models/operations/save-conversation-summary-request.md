# SaveConversationSummaryRequest

## Example Usage

```typescript
import { SaveConversationSummaryRequest } from "bereach/models/operations";

let value: SaveConversationSummaryRequest = {
  profile: "<value>",
  summary: "<value>",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `profile`                                          | *string*                                           | :heavy_check_mark:                                 | LinkedIn profile URL or vanity name of the contact |
| `summary`                                          | *string*                                           | :heavy_check_mark:                                 | Conversation summary text to save                  |
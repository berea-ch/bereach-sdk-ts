# ReviewDraftsRequest

## Example Usage

```typescript
import { ReviewDraftsRequest } from "bereach/models/operations";

let value: ReviewDraftsRequest = {};
```

## Fields

| Field                                                                                                                     | Type                                                                                                                      | Required                                                                                                                  | Description                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `campaignId`                                                                                                              | *string*                                                                                                                  | :heavy_minus_sign:                                                                                                        | The list the drafts belong to. Optional: when omitted it is read from the message ids, which must all belong to one list. |
| `approved`                                                                                                                | *string*[]                                                                                                                | :heavy_minus_sign:                                                                                                        | Message IDs to approve and send                                                                                           |
| `rejected`                                                                                                                | *string*[]                                                                                                                | :heavy_minus_sign:                                                                                                        | Message IDs to reject/cancel                                                                                              |
| `editedMessages`                                                                                                          | Record<string, *string*>                                                                                                  | :heavy_minus_sign:                                                                                                        | Map of messageId to new text (applied before approval)                                                                    |
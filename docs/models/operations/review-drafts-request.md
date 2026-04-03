# ReviewDraftsRequest

## Example Usage

```typescript
import { ReviewDraftsRequest } from "bereach/models/operations";

let value: ReviewDraftsRequest = {
  campaignId: "<id>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `campaignId`                                           | *string*                                               | :heavy_check_mark:                                     | Campaign ID                                            |
| `approved`                                             | *string*[]                                             | :heavy_minus_sign:                                     | Message IDs to approve and send                        |
| `rejected`                                             | *string*[]                                             | :heavy_minus_sign:                                     | Message IDs to reject/cancel                           |
| `editedMessages`                                       | Record<string, *string*>                               | :heavy_minus_sign:                                     | Map of messageId to new text (applied before approval) |
# SendLinkedInMessageResponse

Message sent successfully

## Example Usage

```typescript
import { SendLinkedInMessageResponse } from "bereach/models/operations";

let value: SendLinkedInMessageResponse = {
  success: true,
  messageId: "<id>",
  creditsUsed: 764053,
  retryAfter: 985180,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `messageId`                                                                          | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `duplicate`                                                                          | *boolean*                                                                            | :heavy_minus_sign:                                                                   | True if this action was already executed for the given campaignSlug + target.        |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |
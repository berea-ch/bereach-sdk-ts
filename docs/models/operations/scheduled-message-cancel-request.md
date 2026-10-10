# ScheduledMessageCancelRequest

## Example Usage

```typescript
import { ScheduledMessageCancelRequest } from "bereach/models/operations";

let value: ScheduledMessageCancelRequest = {};
```

## Fields

| Field                                                                                                                                                              | Type                                                                                                                                                               | Required                                                                                                                                                           | Description                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `messageIds`                                                                                                                                                       | *string*[]                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                 | Cancel specific messages                                                                                                                                           |
| `contactIds`                                                                                                                                                       | *string*[]                                                                                                                                                         | :heavy_minus_sign:                                                                                                                                                 | Cancel everything still waiting for these contacts, within the list named by campaignId or campaignSlug when one is given. Prefer messageIds, read from the outbox |
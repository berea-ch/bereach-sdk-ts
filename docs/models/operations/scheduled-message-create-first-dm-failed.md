# ScheduledMessageCreateFirstDmFailed

## Example Usage

```typescript
import { ScheduledMessageCreateFirstDmFailed } from "bereach/models/operations";

let value: ScheduledMessageCreateFirstDmFailed = {
  kind: "failed",
  scheduledMessageId: "<id>",
  reason: "<value>",
  canRequeue: true,
};
```

## Fields

| Field                | Type                 | Required             | Description          |
| -------------------- | -------------------- | -------------------- | -------------------- |
| `kind`               | *"failed"*           | :heavy_check_mark:   | N/A                  |
| `scheduledMessageId` | *string*             | :heavy_check_mark:   | N/A                  |
| `reason`             | *string*             | :heavy_check_mark:   | N/A                  |
| `canRequeue`         | *true*               | :heavy_check_mark:   | N/A                  |
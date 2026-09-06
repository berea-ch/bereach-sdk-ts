# ScheduledMessageCancelRequest

## Example Usage

```typescript
import { ScheduledMessageCancelRequest } from "bereach/models/operations";

let value: ScheduledMessageCancelRequest = {};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `messageIds`                          | *string*[]                            | :heavy_minus_sign:                    | Cancel specific messages              |
| `contactIds`                          | *string*[]                            | :heavy_minus_sign:                    | Cancel all pending for these contacts |
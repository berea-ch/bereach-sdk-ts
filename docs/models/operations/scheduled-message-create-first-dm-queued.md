# ScheduledMessageCreateFirstDmQueued

## Example Usage

```typescript
import { ScheduledMessageCreateFirstDmQueued } from "bereach/models/operations";

let value: ScheduledMessageCreateFirstDmQueued = {
  kind: "queued",
  scheduledMessageId: "<id>",
  why: {
    status: "window",
    detail: "<value>",
    position: null,
    opensAt: "<value>",
    clearsItself: false,
    fixUrl: "https://shy-sermon.biz/",
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `kind`                                                                                          | *"queued"*                                                                                      | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `scheduledMessageId`                                                                            | *string*                                                                                        | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `why`                                                                                           | [operations.ScheduledMessageCreateWhy](../../models/operations/scheduled-message-create-why.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
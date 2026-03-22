# BatchScheduleRequest

## Example Usage

```typescript
import { BatchScheduleRequest } from "bereach/models/operations";

let value: BatchScheduleRequest = {
  scheduledSendAt: "<value>",
};
```

## Fields

| Field                                  | Type                                   | Required                               | Description                            |
| -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- |
| `contactIds`                           | *string*[]                             | :heavy_minus_sign:                     | Schedule all drafts for these contacts |
| `messageIds`                           | *string*[]                             | :heavy_minus_sign:                     | Schedule specific messages             |
| `scheduledSendAt`                      | *string*                               | :heavy_check_mark:                     | ISO datetime for sending               |
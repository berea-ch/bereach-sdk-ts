# Line

What the line did with the approved first messages. Null when nothing was approved.

## Example Usage

```typescript
import { Line } from "bereach/models/operations";

let value: Line = {
  queued: 346044,
  requeued: 413712,
  alreadyQueued: 711739,
  held: 481680,
  skipped: [],
  invitesQueued: 679897,
  accounts: [
    "<value 1>",
  ],
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `queued`                                                                             | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `requeued`                                                                           | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `alreadyQueued`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `held`                                                                               | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `skipped`                                                                            | [operations.ReviewDraftsSkipped](../../models/operations/review-drafts-skipped.md)[] | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `invitesQueued`                                                                      | *number*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `accounts`                                                                           | *string*[]                                                                           | :heavy_check_mark:                                                                   | N/A                                                                                  |
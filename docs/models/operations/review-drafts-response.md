# ReviewDraftsResponse

Review applied

## Example Usage

```typescript
import { ReviewDraftsResponse } from "bereach/models/operations";

let value: ReviewDraftsResponse = {
  success: true,
  approved: 701863,
  rejected: 175028,
  ineligible: {
    approved: [
      {
        id: "<id>",
        currentStatus: "<value>",
      },
    ],
    rejected: [
      {
        id: "<id>",
        currentStatus: null,
      },
    ],
  },
  invitationsApproved: 71942,
  line: {
    queued: 139292,
    requeued: 548203,
    alreadyQueued: 248534,
    held: 183934,
    skipped: [],
    invitesQueued: 157312,
    accounts: [],
  },
  laneBlocked: [],
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `success`                                                                                              | *true*                                                                                                 | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `approved`                                                                                             | *number*                                                                                               | :heavy_check_mark:                                                                                     | Rows now in line: first messages queued, put back or already there, plus connection requests approved. |
| `rejected`                                                                                             | *number*                                                                                               | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `ineligible`                                                                                           | [operations.ReviewDraftsIneligible](../../models/operations/review-drafts-ineligible.md)               | :heavy_check_mark:                                                                                     | Ids that were not in draft, with the status they were in.                                              |
| `invitationsApproved`                                                                                  | *number*                                                                                               | :heavy_check_mark:                                                                                     | Connection requests among the approved ids, handed to the invitation line.                             |
| `line`                                                                                                 | [operations.Line](../../models/operations/line.md)                                                     | :heavy_check_mark:                                                                                     | What the line did with the approved first messages. Null when nothing was approved.                    |
| `laneBlocked`                                                                                          | [operations.LaneBlocked](../../models/operations/lane-blocked.md)[]                                    | :heavy_check_mark:                                                                                     | Rows not approved because their lane is switched off for the list.                                     |
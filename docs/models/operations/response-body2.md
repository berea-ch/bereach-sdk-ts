# ResponseBody2

## Example Usage

```typescript
import { ResponseBody2 } from "bereach/models/operations";

let value: ResponseBody2 = {
  success: true,
  invites: [],
  workspace: {
    tier: "<value>",
    proSeatsIncluded: 669472,
    proSeatsUsed: 313584,
  },
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `success`                                                    | *true*                                                       | :heavy_check_mark:                                           | N/A                                                          |
| `invites`                                                    | [operations.Invite2](../../models/operations/invite2.md)[]   | :heavy_check_mark:                                           | N/A                                                          |
| `workspace`                                                  | [operations.Workspace](../../models/operations/workspace.md) | :heavy_check_mark:                                           | N/A                                                          |
# PullTaskTask

## Example Usage

```typescript
import { PullTaskTask } from "bereach/models/operations";

let value: PullTaskTask = {
  id: "<id>",
  type: "<value>",
  campaignId: "<id>",
  message: "<value>",
  model: "Grand Caravan",
  thinking: "<value>",
  timeoutSeconds: 171471,
  sessionKey: "<value>",
  payload: "<value>",
};
```

## Fields

| Field                     | Type                      | Required                  | Description               |
| ------------------------- | ------------------------- | ------------------------- | ------------------------- |
| `id`                      | *string*                  | :heavy_check_mark:        | N/A                       |
| `type`                    | *string*                  | :heavy_check_mark:        | N/A                       |
| `campaignId`              | *string*                  | :heavy_check_mark:        | N/A                       |
| `message`                 | *string*                  | :heavy_check_mark:        | Task prompt for the agent |
| `model`                   | *string*                  | :heavy_check_mark:        | N/A                       |
| `thinking`                | *string*                  | :heavy_check_mark:        | N/A                       |
| `timeoutSeconds`          | *number*                  | :heavy_check_mark:        | N/A                       |
| `sessionKey`              | *string*                  | :heavy_check_mark:        | N/A                       |
| `payload`                 | *any*                     | :heavy_check_mark:        | N/A                       |
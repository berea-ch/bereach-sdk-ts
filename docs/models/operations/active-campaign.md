# ActiveCampaign

## Example Usage

```typescript
import { ActiveCampaign } from "bereach/models/operations";

let value: ActiveCampaign = {
  id: "<id>",
  name: "<value>",
  type: "<value>",
  status: "<value>",
  context: "<value>",
  stageCounts: {
    contact: 724861,
    lead: 956973,
    qualified: 918675,
    approved: 652290,
    rejected: 735213,
    total: 930890,
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `status`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `context`                                                                                     | *any*                                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `stageCounts`                                                                                 | [operations.AgentSnapshotStageCounts](../../models/operations/agent-snapshot-stage-counts.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
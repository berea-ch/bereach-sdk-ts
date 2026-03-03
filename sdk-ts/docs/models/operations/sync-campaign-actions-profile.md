# SyncCampaignActionsProfile

## Example Usage

```typescript
import { SyncCampaignActionsProfile } from "bereach/models/operations";

let value: SyncCampaignActionsProfile = {
  profile: "<value>",
  actions: [],
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `profile`                                                | *string*                                                 | :heavy_check_mark:                                       | LinkedIn profile URL or URN                              |
| `actions`                                                | [operations.Action](../../models/operations/action.md)[] | :heavy_check_mark:                                       | Action types to mark as completed                        |
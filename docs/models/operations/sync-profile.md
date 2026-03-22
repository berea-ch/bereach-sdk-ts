# SyncProfile

## Example Usage

```typescript
import { SyncProfile } from "bereach/models/operations";

let value: SyncProfile = {
  profile: "<value>",
  actions: [],
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `profile`                                                         | *string*                                                          | :heavy_check_mark:                                                | LinkedIn profile URL or URN                                       |
| `actions`                                                         | [operations.SyncAction](../../models/operations/sync-action.md)[] | :heavy_check_mark:                                                | Action types to mark as completed                                 |
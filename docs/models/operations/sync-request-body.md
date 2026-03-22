# SyncRequestBody

## Example Usage

```typescript
import { SyncRequestBody } from "bereach/models/operations";

let value: SyncRequestBody = {
  profiles: [],
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `profiles`                                                                     | [operations.SyncProfile](../../models/operations/sync-profile.md)[]            | :heavy_check_mark:                                                             | Profiles and actions to mark as completed without performing them on LinkedIn. |
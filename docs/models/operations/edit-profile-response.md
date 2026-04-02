# EditProfileResponse

Profile updated

## Example Usage

```typescript
import { EditProfileResponse } from "bereach/models/operations";

let value: EditProfileResponse = {
  success: true,
  updated: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  synced: [],
  creditsUsed: 328311,
  retryAfter: 132860,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `updated`                                                                            | *string*[]                                                                           | :heavy_check_mark:                                                                   | Fields that were updated on LinkedIn                                                 |
| `synced`                                                                             | *string*[]                                                                           | :heavy_check_mark:                                                                   | Fields that were synced back to the local database                                   |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |
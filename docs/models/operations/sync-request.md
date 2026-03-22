# SyncRequest

## Example Usage

```typescript
import { SyncRequest } from "bereach/models/operations";

let value: SyncRequest = {
  campaignSlug: "<value>",
  body: {
    profiles: [],
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `campaignSlug`                                                             | *string*                                                                   | :heavy_check_mark:                                                         | Campaign identifier                                                        |
| `body`                                                                     | [operations.SyncRequestBody](../../models/operations/sync-request-body.md) | :heavy_check_mark:                                                         | N/A                                                                        |
# GetStatusRequest

## Example Usage

```typescript
import { GetStatusRequest } from "bereach/models/operations";

let value: GetStatusRequest = {
  campaignSlug: "<value>",
  body: {
    profiles: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
};
```

## Fields

| Field                                                                                 | Type                                                                                  | Required                                                                              | Description                                                                           |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| `campaignSlug`                                                                        | *string*                                                                              | :heavy_check_mark:                                                                    | Campaign identifier                                                                   |
| `body`                                                                                | [operations.GetStatusRequestBody](../../models/operations/get-status-request-body.md) | :heavy_check_mark:                                                                    | N/A                                                                                   |
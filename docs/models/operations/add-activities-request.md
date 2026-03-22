# AddActivitiesRequest

## Example Usage

```typescript
import { AddActivitiesRequest } from "bereach/models/operations";

let value: AddActivitiesRequest = {
  id: "<id>",
  body: {
    activities: [
      {
        type: "message",
      },
    ],
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Contact ID                                                                                    |
| `body`                                                                                        | [operations.AddActivitiesRequestBody](../../models/operations/add-activities-request-body.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |
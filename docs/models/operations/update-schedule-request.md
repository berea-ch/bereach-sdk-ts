# UpdateScheduleRequest

## Example Usage

```typescript
import { UpdateScheduleRequest } from "bereach/models/operations";

let value: UpdateScheduleRequest = {
  scheduleId: "<id>",
  body: {
    action: "delete",
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `scheduleId`                                                                                    | *string*                                                                                        | :heavy_check_mark:                                                                              | Schedule ID                                                                                     |
| `body`                                                                                          | [operations.UpdateScheduleRequestBody](../../models/operations/update-schedule-request-body.md) | :heavy_check_mark:                                                                              | N/A                                                                                             |
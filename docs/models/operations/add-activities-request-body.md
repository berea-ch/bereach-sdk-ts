# AddActivitiesRequestBody

## Example Usage

```typescript
import { AddActivitiesRequestBody } from "bereach/models/operations";

let value: AddActivitiesRequestBody = {
  activities: [
    {
      type: "message",
    },
  ],
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `activities`                                                                             | [operations.AddActivitiesActivity](../../models/operations/add-activities-activity.md)[] | :heavy_check_mark:                                                                       | Activities to log                                                                        |
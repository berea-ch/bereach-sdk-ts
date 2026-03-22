# AddActivitiesActivity

## Example Usage

```typescript
import { AddActivitiesActivity } from "bereach/models/operations";

let value: AddActivitiesActivity = {
  type: "qualification",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `type`                                                                         | [operations.AddActivitiesType](../../models/operations/add-activities-type.md) | :heavy_check_mark:                                                             | Activity type                                                                  |
| `content`                                                                      | *string*                                                                       | :heavy_minus_sign:                                                             | Human-readable description of what happened                                    |
| `metadata`                                                                     | *any*                                                                          | :heavy_minus_sign:                                                             | Structured data: postUrl, postAuthor, angle, distance, etc.                    |
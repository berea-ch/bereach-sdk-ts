# ContactsLogActivityActivity

## Example Usage

```typescript
import { ContactsLogActivityActivity } from "bereach/models/operations";

let value: ContactsLogActivityActivity = {
  type: "stage_change",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `type`                                                                                      | [operations.ContactsLogActivityType](../../models/operations/contacts-log-activity-type.md) | :heavy_check_mark:                                                                          | Activity type                                                                               |
| `content`                                                                                   | *string*                                                                                    | :heavy_minus_sign:                                                                          | Human-readable description of what happened                                                 |
| `metadata`                                                                                  | *any*                                                                                       | :heavy_minus_sign:                                                                          | Structured data: postUrl, postAuthor, angle, distance, etc.                                 |
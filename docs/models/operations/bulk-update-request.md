# BulkUpdateRequest

## Example Usage

```typescript
import { BulkUpdateRequest } from "bereach/models/operations";

let value: BulkUpdateRequest = {
  contactIds: [
    "<value 1>",
  ],
  update: {},
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `contactIds`                                           | *string*[]                                             | :heavy_check_mark:                                     | Contact IDs to update                                  |
| `update`                                               | [operations.Update](../../models/operations/update.md) | :heavy_check_mark:                                     | Fields to update on all matching contacts              |
# DeleteRequest

## Example Usage

```typescript
import { DeleteRequest } from "bereach/models/operations";

let value: DeleteRequest = {
  type: "<value>",
};
```

## Fields

| Field                      | Type                       | Required                   | Description                |
| -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| `type`                     | *string*                   | :heavy_check_mark:         | Context type to delete     |
| `scope`                    | *string*                   | :heavy_minus_sign:         | Scope (defaults to "user") |
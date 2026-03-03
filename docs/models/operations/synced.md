# Synced

## Example Usage

```typescript
import { Synced } from "bereach/models/operations";

let value: Synced = {
  profile: "<value>",
  actions: {
    "key": true,
    "key1": false,
    "key2": false,
  },
};
```

## Fields

| Field                     | Type                      | Required                  | Description               |
| ------------------------- | ------------------------- | ------------------------- | ------------------------- |
| `profile`                 | *string*                  | :heavy_check_mark:        | N/A                       |
| `actions`                 | Record<string, *boolean*> | :heavy_check_mark:        | N/A                       |
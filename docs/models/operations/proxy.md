# Proxy

## Example Usage

```typescript
import { Proxy } from "bereach/models/operations";

let value: Proxy = {
  enabled: false,
};
```

## Fields

| Field                                                 | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `enabled`                                             | *boolean*                                             | :heavy_check_mark:                                    | N/A                                                   |
| `mode`                                                | *string*                                              | :heavy_minus_sign:                                    | Which pool the account egresses through.              |
| `country`                                             | *string*                                              | :heavy_minus_sign:                                    | Exit country, ISO alpha-2, uppercase on this surface. |
| `rotationHours`                                       | *number*                                              | :heavy_minus_sign:                                    | How long an exit is held before rotating.             |
# ProxyConfigResidential

## Example Usage

```typescript
import { ProxyConfigResidential } from "bereach/models/operations";

let value: ProxyConfigResidential = {
  mode: "residential",
  country: "Ecuador",
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `mode`                                   | *"residential"*                          | :heavy_check_mark:                       | N/A                                      |
| `country`                                | *string*                                 | :heavy_check_mark:                       | ISO 3166-1 alpha-2 country code.         |
| `city`                                   | *string*                                 | :heavy_minus_sign:                       | City for geo-targeting.                  |
| `rotationHours`                          | *number*                                 | :heavy_minus_sign:                       | Sticky IP rotation in hours (default 1). |
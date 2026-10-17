# ProxyConfigIsp

## Example Usage

```typescript
import { ProxyConfigIsp } from "bereach/models/operations";

let value: ProxyConfigIsp = {
  mode: "isp",
  country: "Bolivia",
  staticIp: "<value>",
  staticPort: 277356,
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `mode`                             | *"isp"*                            | :heavy_check_mark:                 | N/A                                |
| `country`                          | *string*                           | :heavy_check_mark:                 | ISO country code (reference only). |
| `staticIp`                         | *string*                           | :heavy_check_mark:                 | Dedicated static IPv4 address.     |
| `staticPort`                       | *number*                           | :heavy_check_mark:                 | Port for the static IP.            |
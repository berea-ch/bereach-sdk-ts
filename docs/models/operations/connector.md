# Connector

## Example Usage

```typescript
import { Connector } from "bereach/models/operations";

let value: Connector = {
  id: "<id>",
  name: "<value>",
  status: "<value>",
  credentialsId: "<id>",
  lastSeenAt: "<value>",
  lastTaskAt: "<value>",
  createdAt: "1729124753000",
  isOnline: false,
};
```

## Fields

| Field                              | Type                               | Required                           | Description                        |
| ---------------------------------- | ---------------------------------- | ---------------------------------- | ---------------------------------- |
| `id`                               | *string*                           | :heavy_check_mark:                 | N/A                                |
| `name`                             | *string*                           | :heavy_check_mark:                 | N/A                                |
| `status`                           | *string*                           | :heavy_check_mark:                 | online, idle, busy, or offline     |
| `credentialsId`                    | *string*                           | :heavy_check_mark:                 | N/A                                |
| `lastSeenAt`                       | *string*                           | :heavy_check_mark:                 | N/A                                |
| `lastTaskAt`                       | *string*                           | :heavy_check_mark:                 | N/A                                |
| `createdAt`                        | *string*                           | :heavy_check_mark:                 | N/A                                |
| `isOnline`                         | *boolean*                          | :heavy_check_mark:                 | True if lastSeenAt < 5 minutes ago |
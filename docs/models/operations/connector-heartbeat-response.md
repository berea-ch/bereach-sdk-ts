# ConnectorHeartbeatResponse

Heartbeat acknowledged

## Example Usage

```typescript
import { ConnectorHeartbeatResponse } from "bereach/models/operations";

let value: ConnectorHeartbeatResponse = {
  success: true,
  pendingCount: 23563,
  pollIntervalMs: 863814,
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `success`                                                          | *true*                                                             | :heavy_check_mark:                                                 | N/A                                                                |
| `pendingCount`                                                     | *number*                                                           | :heavy_check_mark:                                                 | Number of queued tasks for this credential                         |
| `pollIntervalMs`                                                   | *number*                                                           | :heavy_check_mark:                                                 | Suggested poll interval (5000 when tasks pending, 30000 when idle) |
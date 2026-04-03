# ConnectorHeartbeatRequest

## Example Usage

```typescript
import { ConnectorHeartbeatRequest } from "bereach/models/operations";

let value: ConnectorHeartbeatRequest = {};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `currentTaskId`                                        | *string*                                               | :heavy_minus_sign:                                     | ID of currently executing task (sets status to 'busy') |
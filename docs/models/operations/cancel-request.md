# CancelRequest

## Example Usage

```typescript
import { CancelRequest } from "bereach/models/operations";

let value: CancelRequest = {};
```

## Fields

| Field                                 | Type                                  | Required                              | Description                           |
| ------------------------------------- | ------------------------------------- | ------------------------------------- | ------------------------------------- |
| `messageIds`                          | *string*[]                            | :heavy_minus_sign:                    | Cancel specific messages              |
| `contactIds`                          | *string*[]                            | :heavy_minus_sign:                    | Cancel all pending for these contacts |
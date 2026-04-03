# CancelChainResponse

Chain cancelled

## Example Usage

```typescript
import { CancelChainResponse } from "bereach/models/operations";

let value: CancelChainResponse = {
  success: true,
  tasksCancelled: 212482,
};
```

## Fields

| Field                               | Type                                | Required                            | Description                         |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `success`                           | *true*                              | :heavy_check_mark:                  | N/A                                 |
| `tasksCancelled`                    | *number*                            | :heavy_check_mark:                  | Number of in-flight tasks cancelled |
# SubmitTaskResultRequestBody

## Example Usage

```typescript
import { SubmitTaskResultRequestBody } from "bereach/models/operations";

let value: SubmitTaskResultRequestBody = {};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `status`                                                                                  | [operations.SubmitTaskResultStatus](../../models/operations/submit-task-result-status.md) | :heavy_minus_sign:                                                                        | Intermediate status update (no result yet)                                                |
| `result`                                                                                  | *any*                                                                                     | :heavy_minus_sign:                                                                        | Structured TaskResult on completion                                                       |
| `error`                                                                                   | *string*                                                                                  | :heavy_minus_sign:                                                                        | Error message on failure                                                                  |
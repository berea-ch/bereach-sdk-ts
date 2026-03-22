# ResolveParametersRequest

## Example Usage

```typescript
import { ResolveParametersRequest } from "bereach/models/operations";

let value: ResolveParametersRequest = {
  type: "GEO",
  keywords: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `type`                                                                                 | [operations.ResolveParametersType](../../models/operations/resolve-parameters-type.md) | :heavy_check_mark:                                                                     | Parameter type to resolve                                                              |
| `keywords`                                                                             | *string*                                                                               | :heavy_check_mark:                                                                     | Text to resolve into LinkedIn IDs                                                      |
| `limit`                                                                                | *number*                                                                               | :heavy_minus_sign:                                                                     | Max results (default 10, max 50)                                                       |
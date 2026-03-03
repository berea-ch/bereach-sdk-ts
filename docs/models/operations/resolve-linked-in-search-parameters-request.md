# ResolveLinkedInSearchParametersRequest

## Example Usage

```typescript
import { ResolveLinkedInSearchParametersRequest } from "bereach/models/operations";

let value: ResolveLinkedInSearchParametersRequest = {
  type: "CONNECTIONS",
  keywords: "<value>",
};
```

## Fields

| Field                                                                                                                 | Type                                                                                                                  | Required                                                                                                              | Description                                                                                                           |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                | [operations.ResolveLinkedInSearchParametersType](../../models/operations/resolve-linked-in-search-parameters-type.md) | :heavy_check_mark:                                                                                                    | Parameter type to resolve                                                                                             |
| `keywords`                                                                                                            | *string*                                                                                                              | :heavy_check_mark:                                                                                                    | Text to resolve into LinkedIn IDs                                                                                     |
| `limit`                                                                                                               | *number*                                                                                                              | :heavy_minus_sign:                                                                                                    | Max results (default 10, max 50)                                                                                      |
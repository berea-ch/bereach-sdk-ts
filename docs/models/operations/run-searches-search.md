# RunSearchesSearch

## Example Usage

```typescript
import { RunSearchesSearch } from "bereach/models/operations";

let value: RunSearchesSearch = {
  id: "<id>",
  label: "<value>",
  state: "failed",
  added: 325853,
  queriesRun: 852281,
  queriesPlanned: 336065,
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `id`                                                              | *string*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `label`                                                           | *string*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `state`                                                           | [operations.SearchState](../../models/operations/search-state.md) | :heavy_check_mark:                                                | N/A                                                               |
| `added`                                                           | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `queriesRun`                                                      | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `queriesPlanned`                                                  | *number*                                                          | :heavy_check_mark:                                                | N/A                                                               |
| `note`                                                            | *string*                                                          | :heavy_minus_sign:                                                | N/A                                                               |
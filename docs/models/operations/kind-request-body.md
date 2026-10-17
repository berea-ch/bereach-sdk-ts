# KindRequestBody

## Example Usage

```typescript
import { KindRequestBody } from "bereach/models/operations";

let value: KindRequestBody = {
  said: "<id>",
  industries: [],
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `said`                                                      | *string*                                                    | :heavy_check_mark:                                          | Their own words for this kind, as written.                  |
| `industries`                                                | *string*[]                                                  | :heavy_check_mark:                                          | The LinkedIn industry names such companies are filed under. |
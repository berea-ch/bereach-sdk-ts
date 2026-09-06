# Union

Premium cohorts run both lanes in parallel and merge: the public sweep plus one exact account search, every account row marked lane linkedin. Present when the account arm added people; both spends are receipted.

## Example Usage

```typescript
import { Union } from "bereach/models/operations";

let value: Union = {
  added: 984535,
  linkedinSearches: 305376,
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `added`                                                                  | *number*                                                                 | :heavy_check_mark:                                                       | Rows the connected-account arm added beyond what the public sweep found. |
| `linkedinSearches`                                                       | *number*                                                                 | :heavy_check_mark:                                                       | LinkedIn searches the arm spent.                                         |
# Chain

Turns on a two-step company-discovery search, find matching companies by industry or location, then search the role inside each, for when no company is named yet; once companies are named, use filters.company instead.

## Example Usage

```typescript
import { Chain } from "bereach/models/operations";

let value: Chain = {
  role: "<value>",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `role`                                     | *string*                                   | :heavy_check_mark:                         | Role searched inside each matched company. |
| `companiesLimit`                           | *number*                                   | :heavy_minus_sign:                         | How many companies to search inside.       |
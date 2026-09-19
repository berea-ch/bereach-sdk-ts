# Chain

Turns on a two-step company-discovery search, find matching companies by industry or location, then search the role inside each. ONLY for a request that names no organisation at all: once one is named, it belongs in filters.company and sending this instead searches the wrong thing. Omit it entirely rather than sending it empty.

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
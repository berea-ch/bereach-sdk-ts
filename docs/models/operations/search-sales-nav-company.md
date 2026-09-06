# SearchSalesNavCompany

Current-employer filter (people only). Accepts company names ('Stripe', 'Datadog') OR LinkedIn numeric ids. Server resolves names via typeahead.

## Example Usage

```typescript
import { SearchSalesNavCompany } from "bereach/models/operations";

let value: SearchSalesNavCompany = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `include`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to include. Labels are resolved server-side (no need to call /parameters first). |
| `exclude`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to exclude. Labels are resolved server-side (no need to call /parameters first). |
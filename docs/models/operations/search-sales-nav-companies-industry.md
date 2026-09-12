# SearchSalesNavCompaniesIndustry

Industry filter. Accepts industry names ('Software Development', 'Hospitals and Health Care') OR LinkedIn numeric ids. Server resolves.

## Example Usage

```typescript
import { SearchSalesNavCompaniesIndustry } from "bereach/models/operations";

let value: SearchSalesNavCompaniesIndustry = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `include`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to include. Labels are resolved server-side (no need to call /parameters first). |
| `exclude`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to exclude. Labels are resolved server-side (no need to call /parameters first). |
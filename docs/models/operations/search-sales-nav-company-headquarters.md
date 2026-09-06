# SearchSalesNavCompanyHeadquarters

Where the lead's CURRENT employer is HQ'd (people only). Accepts location names ('France', 'United States') OR LinkedIn geo ids. Distinct from `location` which is the lead's own location — useful for 'sell to UK-headquartered companies regardless of where the buyer lives'.

## Example Usage

```typescript
import { SearchSalesNavCompanyHeadquarters } from "bereach/models/operations";

let value: SearchSalesNavCompanyHeadquarters = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `include`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to include. Labels are resolved server-side (no need to call /parameters first). |
| `exclude`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to exclude. Labels are resolved server-side (no need to call /parameters first). |
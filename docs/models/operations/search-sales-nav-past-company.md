# SearchSalesNavPastCompany

Past-employer filter (people only). Accepts company names ('Stripe') OR LinkedIn numeric ids. The server wraps numeric ids as 'urn:li:organization:<id>' (the wire shape Sales Nav requires) — callers can pass the bare id or the URN.

## Example Usage

```typescript
import { SearchSalesNavPastCompany } from "bereach/models/operations";

let value: SearchSalesNavPastCompany = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `include`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to include. Labels are resolved server-side (no need to call /parameters first). |
| `exclude`                                                                                              | *string*[]                                                                                             | :heavy_minus_sign:                                                                                     | Labels OR numeric IDs to exclude. Labels are resolved server-side (no need to call /parameters first). |
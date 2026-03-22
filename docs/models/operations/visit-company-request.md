# VisitCompanyRequest

## Example Usage

```typescript
import { VisitCompanyRequest } from "bereach/models/operations";

let value: VisitCompanyRequest = {
  companyUrl: "https://thrifty-tomb.org",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `companyUrl`                                                                                                    | *string*                                                                                                        | :heavy_check_mark:                                                                                              | LinkedIn company URL (e.g., 'https://www.linkedin.com/company/openai') or universal name (e.g., 'openai')       |
| `includeWorkplacePolicy`                                                                                        | *boolean*                                                                                                       | :heavy_minus_sign:                                                                                              | Include workplace policy data such as hybrid/remote status and benefits. Costs 1 extra credit (extra API call). |
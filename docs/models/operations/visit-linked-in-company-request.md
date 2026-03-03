# VisitLinkedInCompanyRequest

## Example Usage

```typescript
import { VisitLinkedInCompanyRequest } from "bereach/models/operations";

let value: VisitLinkedInCompanyRequest = {
  companyUrl: "https://variable-co-producer.info",
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `companyUrl`                                                                                                    | *string*                                                                                                        | :heavy_check_mark:                                                                                              | LinkedIn company URL (e.g., 'https://www.linkedin.com/company/openai') or universal name (e.g., 'openai')       |
| `includeWorkplacePolicy`                                                                                        | *boolean*                                                                                                       | :heavy_minus_sign:                                                                                              | Include workplace policy data such as hybrid/remote status and benefits. Costs 1 extra credit (extra API call). |
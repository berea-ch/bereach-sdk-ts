# PublicCompanyRequest

## Example Usage

```typescript
import { PublicCompanyRequest } from "bereach/models/operations";

let value: PublicCompanyRequest = {};
```

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `companyUrl`                                        | *string*                                            | :heavy_minus_sign:                                  | Full public company page URL. Provide this or slug. |
| `slug`                                              | *string*                                            | :heavy_minus_sign:                                  | Company page slug. Provide this or companyUrl.      |
| `country`                                           | *string*                                            | :heavy_minus_sign:                                  | ISO alpha-2 country code for the proxy exit.        |
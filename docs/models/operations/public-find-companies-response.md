# PublicFindCompaniesResponse

Matched companies

## Example Usage

```typescript
import { PublicFindCompaniesResponse } from "bereach/models/operations";

let value: PublicFindCompaniesResponse = {
  source: "public",
  provider: "<value>",
  query: "<value>",
  companies: [
    {
      name: "<value>",
      slug: "<value>",
      companyUrl: "https://humiliating-object.biz/",
      description: "into zowie lively ouch",
    },
  ],
  moreAvailable: true,
};
```

## Fields

| Field                                                                                                                                         | Type                                                                                                                                          | Required                                                                                                                                      | Description                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `source`                                                                                                                                      | [operations.PublicFindCompaniesSource](../../models/operations/public-find-companies-source.md)                                               | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `provider`                                                                                                                                    | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The search provider that answered.                                                                                                            |
| `query`                                                                                                                                       | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The exact query sent, so a thin result set can be read rather than guessed at.                                                                |
| `companies`                                                                                                                                   | [operations.PublicFindCompaniesCompanyResponse](../../models/operations/public-find-companies-company-response.md)[]                          | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `moreAvailable`                                                                                                                               | *boolean*                                                                                                                                     | :heavy_check_mark:                                                                                                                            | Whether asking again with more can still reach rows you have not seen. False means this ask is walked out; say so and do not call more again. |
| `duplicates`                                                                                                                                  | *number*                                                                                                                                      | :heavy_minus_sign:                                                                                                                            | Rows a continuation re-reached and dropped as already delivered. Normal bookkeeping, never a failure.                                         |
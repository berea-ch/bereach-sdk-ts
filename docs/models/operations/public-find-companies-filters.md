# PublicFindCompaniesFilters

Search facets. Provide at least one company-level facet: company, industry, location, or keywords. A role or title cannot select companies.

## Example Usage

```typescript
import { PublicFindCompaniesFilters } from "bereach/models/operations";

let value: PublicFindCompaniesFilters = {};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `title`                                                              | *operations.PublicFindCompaniesTitle*                                | :heavy_minus_sign:                                                   | Role or job title facet. One value or a list of alternatives.        |
| `location`                                                           | *operations.PublicFindCompaniesLocation*                             | :heavy_minus_sign:                                                   | City, region, or country facet. One value or a list of alternatives. |
| `company`                                                            | *operations.PublicFindCompaniesCompanyUnion*                         | :heavy_minus_sign:                                                   | Company name facet. One value or a list of alternatives.             |
| `industry`                                                           | *operations.PublicFindCompaniesIndustry*                             | :heavy_minus_sign:                                                   | Industry facet. One value or a list of alternatives.                 |
| `seniority`                                                          | *operations.PublicFindCompaniesSeniority*                            | :heavy_minus_sign:                                                   | Seniority facet. One value or a list of alternatives.                |
| `keywords`                                                           | *string*                                                             | :heavy_minus_sign:                                                   | Free-text keywords appended to the search query.                     |
| `countryCode`                                                        | *string*                                                             | :heavy_minus_sign:                                                   | ISO alpha-2 country code used to scope results to one country.       |
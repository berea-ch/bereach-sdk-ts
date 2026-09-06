# PublicFindJobsFilters

Search facets. Provide at least one of title, company, location, industry, or keywords.

## Example Usage

```typescript
import { PublicFindJobsFilters } from "bereach/models/operations";

let value: PublicFindJobsFilters = {};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `title`                                                              | *operations.PublicFindJobsTitle*                                     | :heavy_minus_sign:                                                   | Role or job title facet. One value or a list of alternatives.        |
| `location`                                                           | *operations.PublicFindJobsLocation*                                  | :heavy_minus_sign:                                                   | City, region, or country facet. One value or a list of alternatives. |
| `company`                                                            | *operations.PublicFindJobsCompany*                                   | :heavy_minus_sign:                                                   | Company name facet. One value or a list of alternatives.             |
| `industry`                                                           | *operations.PublicFindJobsIndustry*                                  | :heavy_minus_sign:                                                   | Industry facet. One value or a list of alternatives.                 |
| `seniority`                                                          | *operations.PublicFindJobsSeniority*                                 | :heavy_minus_sign:                                                   | Seniority facet. One value or a list of alternatives.                |
| `keywords`                                                           | *string*                                                             | :heavy_minus_sign:                                                   | Free-text keywords appended to the search query.                     |
| `countryCode`                                                        | *string*                                                             | :heavy_minus_sign:                                                   | ISO alpha-2 country code used to scope results to one country.       |
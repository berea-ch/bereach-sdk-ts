# SalesNavigatorSearch

## Overview

### Available Operations

* [search](#search) - Sales Navigator Search — leads (people) & accounts (companies)
* [searchCompanies](#searchcompanies) - Sales Navigator Company/Account Search

## search

# Sales Navigator Search

Search LinkedIn Sales Navigator for leads (people) or accounts (companies). Requires a LinkedIn account with an active Sales Navigator subscription.

## Two ways to search
1. **Structured**: pass `category` + optional `keywords` + filters
2. **URL-based**: pass a Sales Navigator search `url` from your browser — filters are extracted automatically

## Sales Navigator vs Classic search
Sales Navigator returns richer data than classic LinkedIn search:
- **People**: tenure at company/role, premium status, open profile flag, pending invitation status, detailed positions
- **Companies**: headcount (employee count)
- More advanced filters: seniority, function, tenure, include/exclude for company & industry

## Resolving filter IDs
Filters like location, industry, company, and school require LinkedIn numeric IDs. Use `POST /search/linkedin/parameters` to convert text (e.g. "San Francisco") into IDs.

## Pagination
Default page size: 25, max: 25. Use `start` (offset) and `count` to paginate. Check `hasMore` and `paging.total` in the response.

## Credits
1 credit per 10 items returned (minimum 1 if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNav" method="post" path="/search/linkedin/sales-nav" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNavigatorSearch.search({
    category: "people",
    keywords: "developer",
    tenure: [
      {
        min: 3,
      },
    ],
    profileLanguage: [
      "en",
    ],
    start: 0,
    count: 25,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { salesNavigatorSearchSearch } from "bereach/funcs/sales-navigator-search-search.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavigatorSearchSearch(bereach, {
    category: "people",
    keywords: "developer",
    tenure: [
      {
        min: 3,
      },
    ],
    profileLanguage: [
      "en",
    ],
    start: 0,
    count: 25,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("salesNavigatorSearchSearch failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchSalesNavRequest](../../models/operations/search-sales-nav-request.md)                                                                                        | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchSalesNavResponse](../../models/operations/search-sales-nav-response.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.BadRequestError          | 400                             | application/json                |
| errors.UnauthorizedError        | 401                             | application/json                |
| errors.ForbiddenError           | 403                             | application/json                |
| errors.NotFoundError            | 404                             | application/json                |
| errors.ConflictError            | 409                             | application/json                |
| errors.GoneError                | 410                             | application/json                |
| errors.UnprocessableEntityError | 422                             | application/json                |
| errors.TooManyRequestsError     | 429                             | application/json                |
| errors.InternalServerError      | 500                             | application/json                |
| errors.BadGatewayError          | 502                             | application/json                |
| errors.ServiceUnavailableError  | 503                             | application/json                |
| errors.BereachDefaultError      | 4XX, 5XX                        | \*/\*                           |

## searchCompanies

# Sales Navigator Company Search

Search for accounts in LinkedIn Sales Navigator.

## Available filters
| Filter | Type | Description |
|--------|------|-------------|
| `keywords` | string | Search terms |
| `industry` | {include?, exclude?} | Industry IDs with include/exclude |
| `location` | string[] | Geography IDs |
| `companyHeadcount` | string[] | Employee count ranges |
| `companyType` | string[] | Company types |
| `annualRevenue` | string[] | Revenue ranges |

## Credits
1 credit per 10 items returned.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNavCompanies" method="post" path="/search/linkedin/sales-nav/companies" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNavigatorSearch.searchCompanies({
    category: "companies",
    keywords: "SaaS",
    companyHeadcount: [
      "C",
      "D",
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { salesNavigatorSearchSearchCompanies } from "bereach/funcs/sales-navigator-search-search-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavigatorSearchSearchCompanies(bereach, {
    category: "companies",
    keywords: "SaaS",
    companyHeadcount: [
      "C",
      "D",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("salesNavigatorSearchSearchCompanies failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchSalesNavCompaniesRequest](../../models/operations/search-sales-nav-companies-request.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchSalesNavCompaniesResponse](../../models/operations/search-sales-nav-companies-response.md)\>**

### Errors

| Error Type                      | Status Code                     | Content Type                    |
| ------------------------------- | ------------------------------- | ------------------------------- |
| errors.BadRequestError          | 400                             | application/json                |
| errors.UnauthorizedError        | 401                             | application/json                |
| errors.ForbiddenError           | 403                             | application/json                |
| errors.NotFoundError            | 404                             | application/json                |
| errors.ConflictError            | 409                             | application/json                |
| errors.GoneError                | 410                             | application/json                |
| errors.UnprocessableEntityError | 422                             | application/json                |
| errors.TooManyRequestsError     | 429                             | application/json                |
| errors.InternalServerError      | 500                             | application/json                |
| errors.BadGatewayError          | 502                             | application/json                |
| errors.ServiceUnavailableError  | 503                             | application/json                |
| errors.BereachDefaultError      | 4XX, 5XX                        | \*/\*                           |
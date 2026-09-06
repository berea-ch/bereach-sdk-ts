# SalesNav

## Overview

Search LinkedIn Sales Navigator for leads (people) and accounts (companies). Requires an active Sales Navigator subscription.

### Available Operations

* [search](#search) - Sales Navigator Search — leads (people) & accounts (companies)
* [people](#people) - Sales Navigator People/Lead Search
* [companies](#companies) - Sales Navigator Company/Account Search

## search

# Sales Navigator Search

Search LinkedIn Sales Navigator for leads (people) or accounts (companies). Requires a LinkedIn account with an active Sales Navigator subscription.

## Two ways to search
1. **Structured**: pass `category` + optional `keywords` + filters
2. **URL-based**: pass a Sales Navigator search `url` from your browser — filters are extracted automatically

### Accepted `url` shapes
Sales Navigator is a SPA and writes its filter state into the **hash fragment** (`#query=...`), not the search string. The parser accepts both, plus several common paste artefacts:
- `https://www.linkedin.com/sales/search/people#query=(...)&sessionId=...` — what the browser address bar shows (most common)
- `https://www.linkedin.com/sales/search/people?query=(...)` — older / shared-link form
- `/sales/search/lead` and `/sales/search/account` path aliases (LinkedIn uses both)
- Protocol-less paste (`www.linkedin.com/sales/search/people#query=...`)
- Surrounding whitespace, quotes/backticks, `&amp;` from rich-text paste

**Rejected with a clear 400** so you don't get unfiltered results:
- Saved-list URLs (`/sales/lists/people/...`) — these aren't searches; open the list and click "Search" to get a `/sales/search/...` URL
- URLs with no query (`?sessionId=...` only) — copy the URL again **after** filters finish loading
- URLs whose query has no keywords and no filters (`#query=(spellCorrectionEnabled:true)`) — same fix

## Sales Navigator vs Classic search
Sales Navigator returns richer data than classic LinkedIn search:
- **People**: tenure at company/role, premium status, open profile flag, pending invitation status, detailed positions
- **Companies**: headcount (employee count)
- More advanced filters: seniority, function, tenure, include/exclude for company & industry

## Resolving filter IDs
Filters like location, industry, company, and school require LinkedIn numeric IDs. Use `GET /search/linkedin/parameters` to convert text (e.g. "San Francisco") into IDs.

## Pagination
Default page size: 25, max: 25. Use `start` (offset) and `count` to paginate. Check `hasMore` and `paging.total` in the response. When passing `url`, a `?page=N` (or `#…&page=N`) in the URL is honored — explicit `start` still wins if both are provided.

## Credits


## Profile URLs returned
Each item carries `profileUrl` (public `/in/...`) and `salesNavUrl` (`/sales/...`).
Sales Navigator does not return canonical vanity slugs (e.g. `/in/john-doe`) — it returns LinkedIn's encrypted profile id, so `profileUrl` is `https://www.linkedin.com/in/<encrypted-id>` (e.g. `/in/ACwAAA0-26UB...`). These URLs are clickable and redirect to the canonical vanity URL when opened in a browser, and they are accepted anywhere our API takes a profile URL (visit, connect, message, etc.).

### Upgrading to canonical vanity URLs (optional)
To resolve `/in/<encrypted-id>` → `/in/<vanity-slug>` (e.g. `/in/john-doe`), call `POST /resolve/linkedin/profiles` with the URLs, URNs, or raw encrypted ids. The endpoint returns `publicIdentifier` + a canonical `profileUrl`, and returns `publicIdentifier` + a canonical `profileUrl`.

```json
POST /resolve/linkedin/profiles
{
  "inputs": [
    "https://www.linkedin.com/in/ACwAAA0-26UBSvneYv1dZ1sfAT_NZHjmOb5qk2s",
    "urn:li:fsd_profile:ACwAAAaK0QIBxcI7cceYW8eas-3uVGwgOTW8s_k"
  ]
}
```

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNav" method="post" path="/search/linkedin/sales-nav" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNav.search({
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
import { salesNavSearch } from "bereach/funcs/sales-nav-search.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavSearch(bereach, {
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
    console.log("salesNavSearch failed:", res.error);
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

## people

# Sales Navigator People Search

Search for leads in LinkedIn Sales Navigator with advanced filters. Returns enriched profile data including tenure, premium status, and open profile flag.

## Available filters
| Filter | Type | Description |
|--------|------|-------------|
| `keywords` | string | Search terms |
| `title` | string | Job title keywords |
| `company` | {include?, exclude?} | Company IDs with include/exclude |
| `industry` | {include?, exclude?} | Industry IDs with include/exclude |
| `location` | string[] | Geography IDs |
| `seniority` | string[] | Seniority levels (1-10) |
| `function` | string[] | Job function IDs |
| `tenure` | {min?, max?}[] | Years at current company |
| `profileLanguage` | string[] | Profile language codes |
| `connectionDegree` | string[] | Network distance (1, 2, 3) |
| `school` | string[] | School IDs |
| `yearsOfExperience` | string[] | Experience ranges |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Sales Navigator lead ID |
| `name`, `firstName`, `lastName` | string | Name |
| `memberUrn` | string | LinkedIn member URN |
| `profileUrn` | string | Canonical profile URN (`urn:li:fsd_profile:ACoA...` or `urn:li:fsd_profile:ACwA...`) — use directly with visit/connect/message endpoints |
| `profileUrl` | string | Public LinkedIn profile URL `https://www.linkedin.com/in/<encrypted-id>`. Sales Nav does not expose canonical vanity slugs — open in a browser and LinkedIn redirects to `/in/<vanity-name>`. To resolve programmatically, call `POST /resolve/linkedin/profiles`. |
| `salesNavUrl` | string | Sales Navigator lead URL |
| `networkDistance` | string | Connection degree |
| `premium` | boolean | LinkedIn Premium subscriber |
| `openProfile` | boolean | Accepts free InMail |
| `pendingInvitation` | boolean | Connection request already sent |
| `currentPositions` | array | With company, role, tenure details |

## Credits


## JSON validity (critical)
Every array field (seniority, function, location, companyHeadcount, companyType, connectionDegree, yearsOfExperience, profileLanguage, school) MUST be a valid JSON array of double-quoted strings, e.g. `["Director","Vice President"]`. Never pipe-separated prose (`Director | Vice President`), never unquoted values (`United States`), never merge multiple options into one element. Malformed JSON means the filter is dropped and the search runs unfiltered.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNavPeople" method="post" path="/search/linkedin/sales-nav/people" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNav.people({
    keywords: "developer",
    tenure: [
      {
        min: 5,
      },
    ],
    profileLanguage: [
      "en",
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
import { salesNavPeople } from "bereach/funcs/sales-nav-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavPeople(bereach, {
    keywords: "developer",
    tenure: [
      {
        min: 5,
      },
    ],
    profileLanguage: [
      "en",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("salesNavPeople failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchSalesNavPeopleRequest](../../models/operations/search-sales-nav-people-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchSalesNavPeopleResponse](../../models/operations/search-sales-nav-people-response.md)\>**

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

## companies

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

## Credits


### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNavCompanies" method="post" path="/search/linkedin/sales-nav/companies" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNav.companies({
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
import { salesNavCompanies } from "bereach/funcs/sales-nav-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavCompanies(bereach, {
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
    console.log("salesNavCompanies failed:", res.error);
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
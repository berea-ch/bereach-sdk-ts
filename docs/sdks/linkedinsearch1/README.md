# LinkedInSearch

## Overview

### Available Operations

* [search](#search) - Unified LinkedIn Search — posts, people, companies, jobs
* [searchCompanies](#searchcompanies) - Search LinkedIn Companies

## search

# Unified LinkedIn Search

This is the **all-in-one** search endpoint. It accepts any of the 4 categories (posts, people, companies, jobs) and returns structured results.

## When to use this endpoint
Use this endpoint when you need to search across categories dynamically (e.g. the user chooses the category at runtime). For a simpler interface with category-specific documentation, use the dedicated endpoints:
- `POST /search/linkedin/posts` — search posts
- `POST /search/linkedin/people` — search people
- `POST /search/linkedin/companies` — search companies
- `POST /search/linkedin/jobs` — search jobs
- `POST /search/linkedin/url` — search by pasting a LinkedIn search URL

## Two ways to search
1. **Structured**: pass `category` + `keywords` + optional filters
2. **URL-based**: pass a LinkedIn search `url` — the endpoint parses it automatically

Explicit parameters always override URL-derived values.

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax for precise matching:
- **Exact phrase**: wrap in double quotes — `"outreach automation"` matches only that exact phrase
- **AND**: both terms required — `outreach AND linkedin` (default when terms are space-separated)
- **OR**: either term — `CEO OR founder OR owner`
- **NOT**: exclude — `manager NOT assistant`
- **Parentheses**: group — `(CEO OR CTO) AND SaaS`

Operators must be **UPPERCASE** (`AND`, `OR`, `NOT`). Lowercase is treated as plain text. Wildcards (`*`) and `+`/`-` are not supported. Precedence: Quotes → Parentheses → NOT → AND → OR.

Without quotes, a multi-word query like `outreach automation` is treated as `outreach AND automation`, which may return broad results. Use `"outreach automation"` for exact matching.

## Resolving filter IDs
Many filters (location, industry, company, school) require LinkedIn numeric IDs. Use `POST /search/linkedin/parameters` to convert text (e.g. "San Francisco") into IDs (e.g. "103644278").

## Pagination
Use `start` (offset, default 0) and `count` (page size, default 10, max 50). The response includes `paging.total` and `hasMore` to control iteration.

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="search" method="post" path="/search/linkedin" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedInSearch.search({
    category: "people",
    keywords: "software engineer",
    connectionDegree: [
      "F",
      "S",
    ],
    location: [
      "103644278",
    ],
    industry: [
      "4",
      "6",
    ],
    start: 0,
    count: 10,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedInSearchSearch } from "bereach/funcs/linked-in-search-search.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedInSearchSearch(bereach, {
    category: "people",
    keywords: "software engineer",
    connectionDegree: [
      "F",
      "S",
    ],
    location: [
      "103644278",
    ],
    industry: [
      "4",
      "6",
    ],
    start: 0,
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedInSearchSearch failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchRequest](../../models/operations/search-request.md)                                                                                                          | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchResponse](../../models/operations/search-response.md)\>**

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

# Search LinkedIn Companies

Find companies on LinkedIn by name, industry, location, and employee count. Returns structured company data including name, industry, location, and follower count.

## Parameters
- **keywords** (optional): Search terms matched against company name, description, and specialties

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"artificial intelligence"` — matches only that exact phrase
- **AND**: `fintech AND payments` — both terms required (spaces default to AND)
- **OR**: `SaaS OR "cloud computing"` — either term
- **NOT**: `consulting NOT staffing` — exclude unwanted terms
- **Parentheses**: `(AI OR ML) AND healthcare` — group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
| Filter | Type | Description | Resolve IDs via |
|--------|------|-------------|------------------|
| `location` | string[] | HQ geo IDs | `/search/linkedin/parameters` type=`GEO` |
| `industry` | string[] | Industry IDs | `/search/linkedin/parameters` type=`INDUSTRY` |
| `companySize` | string[] | Employee count codes (see below) | — |

### Company size codes
| Code | Employees |
|------|-----------|
| `A` | 1–10 |
| `B` | 11–50 |
| `C` | 51–200 |
| `D` | 201–500 |
| `E` | 501–1,000 |
| `F` | 1,001–5,000 |
| `G` | 5,001–10,000 |
| `H` | 10,001+ |
| `I` | Self-employed |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Company display name |
| `profileUrl` | string | LinkedIn company page URL |
| `summary` | string\|null | Company tagline/description |
| `industry` | string\|null | Primary industry |
| `location` | string\|null | HQ location |
| `followersCount` | number\|null | Number of LinkedIn followers |

## Pagination
- Default page size: 10, max: 50
- Use `start` + `count` to paginate. Check `hasMore` for more pages.

## Example workflows
1. **Market research**: Search by industry + location → map the competitive landscape
2. **Sales targeting**: Search by industry + size → build a list of target accounts
3. **Partnership discovery**: Search by keywords + location → find potential partners

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchCompanies" method="post" path="/search/linkedin/companies" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedInSearch.searchCompanies({
    keywords: "AI startup",
    location: [
      "103644278",
    ],
    companySize: [
      "B",
      "C",
    ],
    start: 0,
    count: 10,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedInSearchSearchCompanies } from "bereach/funcs/linked-in-search-search-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedInSearchSearchCompanies(bereach, {
    keywords: "AI startup",
    location: [
      "103644278",
    ],
    companySize: [
      "B",
      "C",
    ],
    start: 0,
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedInSearchSearchCompanies failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchCompaniesRequest](../../models/operations/search-companies-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchCompaniesResponse](../../models/operations/search-companies-response.md)\>**

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
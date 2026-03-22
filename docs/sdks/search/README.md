# Search

## Overview

Search LinkedIn for posts, people, companies, and jobs. Includes parameter resolution (typeahead) for converting text to LinkedIn IDs.

### Available Operations

* [search](#search) - Unified LinkedIn Search — posts, people, companies, jobs
* [posts](#posts) - Search LinkedIn Posts
* [people](#people) - Search LinkedIn People
* [companies](#companies) - Search LinkedIn Companies
* [jobs](#jobs) - Search LinkedIn Jobs
* [byUrl](#byurl) - Search LinkedIn by URL
* [resolveParameters](#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)

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
  const result = await bereach.search.search({
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
import { searchSearch } from "bereach/funcs/search-search.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchSearch(bereach, {
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
    console.log("searchSearch failed:", res.error);
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

## posts

# Search LinkedIn Posts

Search LinkedIn's content index for posts matching your keywords and filters. Returns structured post data including full text, engagement metrics, author info, and URLs.

## Required parameters
- **keywords** (string, required): The search terms to match against post content. Examples: `"AI automation"`, `"remote work trends"`, `"SaaS growth strategies"`.

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"outreach automation"` — matches only that exact phrase
- **AND**: `AI AND marketing` — both terms required (spaces default to AND)
- **OR**: `"growth hacking" OR "growth marketing"` — either term
- **NOT**: `outreach NOT webinar` — exclude unwanted terms
- **Parentheses**: `(AI OR ML) AND "case study"` — group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
| Filter | Type | Description |
|--------|------|-------------|
| `sortBy` | `"relevance"` \| `"date"` | Sort by relevance (default) or most recent first |
| `datePosted` | `"past-24h"` \| `"past-week"` \| `"past-month"` | Filter by publication recency |
| `contentType` | `"images"` \| `"videos"` \| `"documents"` | Filter by media type |
| `authorIndustry` | string[] | Author's industry IDs (resolve via `/search/linkedin/parameters` with type=`INDUSTRY`) |
| `authorCompany` | string[] | Author's company IDs (resolve via `/search/linkedin/parameters` with type=`COMPANY`) |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `postUrl` | string | Direct URL to the LinkedIn post |
| `text` | string | Full post text content |
| `date` | number | Publication timestamp (ms since epoch) |
| `likesCount` | number | Total reactions |
| `commentsCount` | number | Total comments |
| `sharesCount` | number | Total shares/reposts |
| `author.name` | string | Author's display name |
| `author.profileUrl` | string | Author's LinkedIn profile URL |
| `author.headline` | string | Author's headline |
| `author.isCompany` | boolean | Whether the author is a company page |
| `isRepost` | boolean | Whether this is a repost of another post |

## Pagination
- Default page size: 10, max: 50
- Use `start` + `count` to paginate: `start=0, count=10` → page 1, `start=10, count=10` → page 2
- Check `hasMore` in the response to know if more pages exist
- `paging.total` gives the estimated total number of results

## Example workflows
1. **Content research**: Search for trending topics → analyze top posts → extract engagement patterns
2. **Lead generation**: Search for posts about problems your product solves → extract author profiles
3. **Competitive intelligence**: Search for competitor mentions → track sentiment and engagement

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchPosts" method="post" path="/search/linkedin/posts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.posts({
    keywords: "AI automation",
    sortBy: "date",
    datePosted: "past-week",
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
import { searchPosts } from "bereach/funcs/search-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPosts(bereach, {
    keywords: "AI automation",
    sortBy: "date",
    datePosted: "past-week",
    start: 0,
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchPostsRequest](../../models/operations/search-posts-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchPostsResponse](../../models/operations/search-posts-response.md)\>**

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

# Search LinkedIn People

Find professionals on LinkedIn by name, title, company, location, industry, and more. Returns structured profile data including name, headline, current positions, and connection degree.

## Parameters
- **keywords** (optional): Search terms matched against name, headline, company, skills, and bio
- You can search by filters alone (no keywords) — e.g. find all 2nd-degree connections in Paris

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"product manager"` — matches only that exact title
- **AND**: `engineer AND startup` — both terms required (spaces default to AND)
- **OR**: `CEO OR founder OR CTO` — any of the terms
- **NOT**: `manager NOT assistant` — exclude unwanted terms
- **Parentheses**: `(CEO OR CTO) AND SaaS` — group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
| Filter | Type | Description | Resolve IDs via |
|--------|------|-------------|------------------|
| `connectionDegree` | `["F"\|"S"\|"O"]` | Connection level: F=1st, S=2nd, O=3rd+ | — |
| `firstName` | string | Exact first name match | — |
| `lastName` | string | Exact last name match | — |
| `title` | string | Current job title (supports `\|` OR syntax: `"CEO\|CTO"`) | — |
| `connectionOf` | string | Profile URN — find their connections | — |
| `profileLanguage` | string[] | ISO 639-1 codes: `["en","fr"]` | — |
| `location` | string[] | Geo IDs | `/search/linkedin/parameters` type=`GEO` |
| `industry` | string[] | Industry IDs | `/search/linkedin/parameters` type=`INDUSTRY` |
| `currentCompany` | string[] | Company IDs (current employer) | `/search/linkedin/parameters` type=`COMPANY` |
| `pastCompany` | string[] | Company IDs (past employer) | `/search/linkedin/parameters` type=`COMPANY` |
| `school` | string[] | School/university IDs | `/search/linkedin/parameters` type=`SCHOOL` |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Full display name |
| `profileUrl` | string | LinkedIn profile URL |
| `headline` | string\|null | Professional headline |
| `location` | string\|null | Geographic location |
| `profilePicture` | string\|null | Profile photo URL |
| `networkDistance` | string\|null | `DISTANCE_1`, `DISTANCE_2`, `DISTANCE_3`, or `OUT_OF_NETWORK` |
| `currentPositions` | array | Current job positions with `company` and `role` |

## Pagination
- Default page size: 10, max: 50
- Use `start` + `count` to paginate. Check `hasMore` for more pages.
- LinkedIn caps total visible results at ~1,000 for most searches.

## Example workflows
1. **Prospect list building**: Search by title + location + industry → build a targeted outreach list
2. **Recruiting**: Search by title + company + school → find qualified candidates
3. **Network mapping**: Search `connectionOf` + filters → explore someone's network

## Multi-step workflow with filter ID resolution
```
Step 1: POST /search/linkedin/parameters { type: 'GEO', keywords: 'San Francisco' }
        → returns [{ id: '102277331', title: 'San Francisco, CA' }]
Step 2: POST /search/linkedin/parameters { type: 'COMPANY', keywords: 'Google' }
        → returns [{ id: '1441', title: 'Google' }]
Step 3: POST /search/linkedin/people { keywords: 'product manager', location: ['102277331'], currentCompany: ['1441'] }
        → returns matching people
```

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchPeople" method="post" path="/search/linkedin/people" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.people({
    keywords: "product manager",
    connectionDegree: [
      "S",
    ],
    location: [
      "103644278",
    ],
    currentCompany: [
      "1441",
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
import { searchPeople } from "bereach/funcs/search-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchPeople(bereach, {
    keywords: "product manager",
    connectionDegree: [
      "S",
    ],
    location: [
      "103644278",
    ],
    currentCompany: [
      "1441",
    ],
    start: 0,
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchPeople failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchPeopleRequest](../../models/operations/search-people-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchPeopleResponse](../../models/operations/search-people-response.md)\>**

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
  const result = await bereach.search.companies({
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
import { searchCompanies } from "bereach/funcs/search-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchCompanies(bereach, {
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
    console.log("searchCompanies failed:", res.error);
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

## jobs

# Search LinkedIn Jobs

Find job listings on LinkedIn by keywords, location, job type, experience level, and workplace type.

## Parameters
- **keywords** (optional): Search terms matched against job title, company name, and description

## Keyword syntax (Boolean operators)
Keywords support LinkedIn Boolean search syntax:
- **Exact phrase**: `"frontend engineer"` — matches only that exact title
- **AND**: `React AND TypeScript` — both terms required (spaces default to AND)
- **OR**: `"frontend engineer" OR "front-end developer"` — either term
- **NOT**: `engineer NOT intern` — exclude unwanted terms
- **Parentheses**: `(React OR Vue) AND "senior engineer"` — group logic

Operators must be **UPPERCASE**. Precedence: Quotes > Parentheses > NOT > AND > OR.

## Available filters
| Filter | Type | Description | Resolve IDs via |
|--------|------|-------------|------------------|
| `location` | string[] | Geo IDs | `/search/linkedin/parameters` type=`GEO` |
| `datePosted` | string | `"past-24h"` \| `"past-week"` \| `"past-month"` | — |
| `sortBy` | string | `"relevance"` \| `"date"` | — |
| `jobType` | string[] | Employment type codes (see below) | — |
| `experienceLevel` | string[] | Seniority codes (see below) | — |
| `workplaceType` | string[] | Work location codes (see below) | — |

### Job type codes
| Code | Type |
|------|------|
| `F` | Full-time |
| `P` | Part-time |
| `C` | Contract |
| `T` | Temporary |
| `I` | Internship |
| `V` | Volunteer |
| `O` | Other |

### Experience level codes
| Code | Level |
|------|-------|
| `1` | Internship |
| `2` | Entry level |
| `3` | Associate |
| `4` | Mid-Senior level |
| `5` | Director |
| `6` | Executive |

### Workplace type codes
| Code | Type |
|------|------|
| `1` | On-site |
| `2` | Remote |
| `3` | Hybrid |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Job title |
| `company` | string\|null | Hiring company name |
| `companyUrl` | string\|null | Company LinkedIn page URL |
| `companyLogo` | string\|null | Company logo URL |
| `location` | string\|null | Job location |
| `workplaceType` | string\|null | On-site / Remote / Hybrid |
| `postedAt` | string\|null | Human-readable posting time (e.g. `"2 days ago"`) |
| `jobUrl` | string | Direct URL to the job listing |
| `listingId` | string | LinkedIn job listing ID |

## Pagination
- Default page size: 10, max: 50
- Use `start` + `count` to paginate. Check `hasMore` for more pages.

## Example workflows
1. **Job monitoring**: Search by title + location → track new openings in your area
2. **Competitive hiring analysis**: Search by company keywords → see what roles competitors are hiring for
3. **Market demand research**: Search by skills → gauge demand for specific expertise

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchJobs" method="post" path="/search/linkedin/jobs" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.jobs({
    keywords: "frontend engineer",
    location: [
      "102095887",
    ],
    jobType: [
      "F",
    ],
    experienceLevel: [
      "3",
      "4",
    ],
    workplaceType: [
      "2",
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
import { searchJobs } from "bereach/funcs/search-jobs.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchJobs(bereach, {
    keywords: "frontend engineer",
    location: [
      "102095887",
    ],
    jobType: [
      "F",
    ],
    experienceLevel: [
      "3",
      "4",
    ],
    workplaceType: [
      "2",
    ],
    start: 0,
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchJobs failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchJobsRequest](../../models/operations/search-jobs-request.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchJobsResponse](../../models/operations/search-jobs-response.md)\>**

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

## byUrl

# Search LinkedIn by URL

Paste any LinkedIn search URL and the endpoint will automatically extract the category, keywords, and all filters from it, then execute the search and return structured results.

## When to use this endpoint
- A user gives you a LinkedIn search URL and you want to get the results programmatically
- You want to replicate a search the user performed in their browser
- You want to automate searches based on bookmarked LinkedIn search URLs

## Supported URL formats
The endpoint supports all standard LinkedIn search URLs:
- `https://www.linkedin.com/search/results/people/?keywords=engineer`
- `https://www.linkedin.com/search/results/content/?keywords=AI&sortBy=%22date_posted%22`
- `https://www.linkedin.com/search/results/companies/?keywords=startup&companyHqGeo=%5B%22103644278%22%5D`
- `https://www.linkedin.com/jobs/search/?keywords=frontend&location=Paris`
- `https://www.linkedin.com/search/results/all/?keywords=test` (treated as people search)

## URL path → Category mapping
| URL path segment | Category |
|------------------|----------|
| `/results/content/` | posts |
| `/results/people/` | people |
| `/results/companies/` | companies |
| `/results/all/` | people |
| `/jobs/search/` | jobs |

## Extracted parameters
The following URL query parameters are parsed and mapped to search filters:
- `keywords` → keywords
- `network` → connectionDegree (people)
- `geoUrn` / `companyHqGeo` → location
- `industry` → industry
- `company` / `currentCompany` → currentCompany
- `pastCompany` → pastCompany
- `school` → school
- `profileLanguage` → profileLanguage
- `connectionOf` → connectionOf
- `firstName` / `lastName` → firstName / lastName
- `title` → title
- `companySize` → companySize (companies)
- `sortBy` → sortBy
- `datePosted` → datePosted
- `f_TPR` → datePosted (jobs)
- `f_JT` → jobType (jobs)
- `f_E` → experienceLevel (jobs)
- `f_WT` → workplaceType (jobs)

## Pagination override
You can optionally pass `start` and `count` to override the pagination embedded in the URL.

## Credits
1 credit per 20 items returned (minimum 1 credit if any results, 0 if empty).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchByUrl" method="post" path="/search/linkedin/url" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.byUrl({
    url: "https://www.linkedin.com/search/results/people/?keywords=software%20engineer&network=%5B%22S%22%5D&origin=FACETED_SEARCH",
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
import { searchByUrl } from "bereach/funcs/search-by-url.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchByUrl(bereach, {
    url: "https://www.linkedin.com/search/results/people/?keywords=software%20engineer&network=%5B%22S%22%5D&origin=FACETED_SEARCH",
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchByUrl failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchByUrlRequest](../../models/operations/search-by-url-request.md)                                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchByUrlResponse](../../models/operations/search-by-url-response.md)\>**

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

## resolveParameters

# Resolve Search Parameters

Converts human-readable text into LinkedIn numeric IDs required by search filters. This is a **prerequisite step** before using location, industry, company, or school filters in any search endpoint.

## Supported types
| Type | Description | Use with filter |
|------|-------------|------------------|
| `GEO` | Geographic locations (cities, regions, countries) | `location` filter in people, companies, jobs |
| `COMPANY` | Companies and organizations | `currentCompany`, `pastCompany`, `authorCompany` |
| `INDUSTRY` | Industries and sectors | `industry`, `authorIndustry` |
| `SCHOOL` | Schools and universities | `school` filter in people search |
| `CONNECTIONS` | Your LinkedIn connections by name | Identify connection URNs |
| `PEOPLE` | Any LinkedIn user by name | Identify profile URNs for `connectionOf` |

## How to use
```
Step 1: GET /search/linkedin/parameters?type=GEO&keywords=Paris
        → [{ id: '105015875', title: 'Paris, Île-de-France, France', type: 'GEO' }]
Step 2: POST /search/linkedin/people { location: ['105015875'], keywords: 'engineer' }
        → returns engineers in Paris
```

## Response format
Each item contains `id` (the LinkedIn numeric ID to use in filters), `title` (human-readable label), and `type` (the parameter type).

## Tips
- Use short, specific keywords for best results (e.g. `"Paris"` not `"Paris, France"`)
- The API returns up to `limit` results (default 10, max 50)
- Results are ranked by relevance
- IDs are stable — you can cache them for repeated searches

**Note**: This is a GET endpoint. Pass `type`, `keywords`, and `limit` as query parameters.
Example: `GET /search/linkedin/parameters?type=GEO&keywords=Paris&limit=5`

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resolveParameters" method="get" path="/search/linkedin/parameters" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.resolveParameters({
    type: "PEOPLE",
    keywords: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchResolveParameters } from "bereach/funcs/search-resolve-parameters.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchResolveParameters(bereach, {
    type: "PEOPLE",
    keywords: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchResolveParameters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResolveParametersRequest](../../models/operations/resolve-parameters-request.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ResolveParametersResponse](../../models/operations/resolve-parameters-response.md)\>**

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
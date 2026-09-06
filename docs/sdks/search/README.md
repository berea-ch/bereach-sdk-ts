# Search

## Overview

Search LinkedIn for posts, people, companies, and jobs. Includes parameter resolution (typeahead) for converting text to LinkedIn IDs.

### Available Operations

* [employees](#employees) - Search people at a company
* [posts](#posts) - Search LinkedIn Posts
* [people](#people) - Search LinkedIn People
* [companies](#companies) - Search LinkedIn Companies
* [jobs](#jobs) - Search LinkedIn Jobs
* [byUrl](#byurl) - Search LinkedIn by URL
* [listSalesNavFilters](#listsalesnavfilters) - List the Sales Navigator filters available for this seat
* [listSalesNavPersonas](#listsalesnavpersonas) - List the user's saved Sales Navigator personas
* [listSalesNavSavedSearches](#listsalesnavsavedsearches) - List the user's saved Sales Navigator searches
* [searchParameters](#searchparameters) - Turn text into the ids LinkedIn filters take
* [resolveProfiles](#resolveprofiles) - Upgrade encrypted or Sales Navigator profile links to canonical ones

## employees

People currently associated with a company on LinkedIn. Pass a company URL, vanity slug, or name. Implemented via the cookie people-search path with `currentCompany` (HTML pages of ~10, accumulated to `count`). Optional `keywords` narrows within that company. Same result shape as search people.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchEmployees" method="post" path="/search/linkedin/employees" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.employees({
    company: "https://www.linkedin.com/company/stripe/",
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
import { searchEmployees } from "bereach/funcs/search-employees.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchEmployees(bereach, {
    company: "https://www.linkedin.com/company/stripe/",
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchEmployees failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchEmployeesRequest](../../models/operations/search-employees-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchEmployeesResponse](../../models/operations/search-employees-response.md)\>**

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
| `authorJobTitle` | string[] | The author's job title, free text. The strongest filter here: two different titles return sets of authors that do not overlap, so asking twice reaches twice as many people |
| `postedBy` | string[] | Restrict to your own network: `first` or `following`. Far fewer results by nature |
| `contentType` | `"images"` \| `"videos"` \| `"documents"` | Filter by media type |
| `authorIndustry` | string[] | Author's industry IDs (resolve via `/search/linkedin/parameters` with type=`INDUSTRY`) |
| `authorCompany` | string[] | Author's company IDs (resolve via `/search/linkedin/parameters` with type=`COMPANY`) |
| `datePosted` | `"past-24h"` \| `"past-week"` \| `"past-month"` | Filter by recency window. On a high-volume query the newest posts are shared across windows, so the first page can look unchanged while the narrower window holds fewer results |

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
    authorJobTitle: [
      "head of engineering",
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
    authorJobTitle: [
      "head of engineering",
    ],
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

Find professionals on LinkedIn by name, title, company, location, industry, and more. Returns structured profile data including name, headline, current positions, connection degree, profile picture, **plus 2026-06-03 enrichments**: `nameMatch` (true when the result matched on literal name — strong personhood signal), `badgeText` (Top Voice / Premium / Verified / Influencer — qualifier weight), `ringStatus` (OPEN_TO_WORK / HIRING — open intent signals you can directly target), `summary` (additional snippet beyond headline), `actorInsights` (LinkedIn-curated context like 'X mutual connections', 'Follows {company}' — use directly in personalised outreach openers).

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
Pass HUMAN LABELS for location / industry / currentCompany / pastCompany / school — the server resolves them to LinkedIn IDs via typeahead. Numeric IDs pass through unchanged if you already have them.

| Filter | Type | Description |
|--------|------|-------------|
| `connectionDegree` | `["F"\|"S"\|"O"]` | Connection level: F=1st, S=2nd, O=3rd+ |
| `firstName` | string | Exact first name match |
| `lastName` | string | Exact last name match |
| `title` | string | Current job title (supports `\|` OR syntax: `"CEO\|CTO"`) |
| `connectionOf` | string | Profile URN — find their connections |
| `followersOf` | string[] | Profile URNs — find a creator's followers |
| `openToVolunteering` | boolean | Only people open to volunteering |
| `serviceCategories` | string[] | Service-Marketplace category names |
| `profileLanguage` | string[] | ISO 639-1 codes: `["en","fr"]` |
| `location` | string[] | Geo labels (e.g. `["Paris","France"]`) — resolved server-side |
| `industry` | string[] | Industry labels (e.g. `["Software Development"]`) — resolved server-side |
| `currentCompany` | string[] | Company labels (e.g. `["Stripe","Datadog"]`) — resolved server-side |
| `pastCompany` | string[] | Company labels — resolved server-side |
| `school` | string[] | School/university labels — resolved server-side |

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
- Paginate via `start` + `count`; check `hasMore` for more pages.

## Example workflows
1. **Prospect list building**: Search by title + location + industry → build a targeted outreach list
2. **Recruiting**: Search by title + company + school → find people who match
3. **Network mapping**: Search `connectionOf` + filters → explore someone's network

## Workflow — pass labels directly
```
POST /search/linkedin/people {
  keywords: 'product manager',
  location: ['San Francisco'],
  currentCompany: ['Google']
}
→ server resolves labels → matching people
```
Only call `/search/linkedin/parameters` when you need to EXPLORE available values ("what are the canonical industry buckets?"), never as a prerequisite to a search.

## Credits


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

Find companies on LinkedIn by name, industry, location, and employee count. Returns structured company data: name, profileUrl, summary, industry, location, followersCount, logoUrl. To read a single result in more depth, pass its profileUrl to **publicCompany**, which adds the full description, follower and employee counts, the website, and recent posts. Detailed firmographics (headquarter address, founding year, specialities, verification status, call to action) are not available from either surface, so do not promise them.

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
Pass HUMAN LABELS for location / industry — the server resolves them to LinkedIn IDs via typeahead. Numeric IDs pass through unchanged if you already have them.

| Filter | Type | Description |
|--------|------|-------------|
| `location` | string[] | HQ geo labels (e.g. `["Paris","France"]`) — resolved server-side |
| `industry` | string[] | Industry labels (e.g. `["Software Development"]`) — resolved server-side |
| `companySize` | string[] | Employee count codes (see below) |

### Company size codes
| Code | Employees |
|------|-----------|
| `A` | 1 |
| `B` | 2-10 |
| `C` | 11-50 |
| `D` | 51-200 |
| `E` | 201-500 |
| `F` | 501-1,000 |
| `G` | 1,001-5,000 |
| `H` | 5,001-10,000 |
| `I` | 10,001+ |

## Response fields (per item)
| Field | Type | Description |
|-------|------|-------------|
| `name` | string | Company display name |
| `profileUrl` | string | LinkedIn company page URL |
| `summary` | string\|null | Company tagline/description |
| `industry` | string\|null | Primary industry |
| `location` | string\|null | HQ location |
| `followersCount` | number\|null | Number of LinkedIn followers |
| `logoUrl` | string\|null | Company logo, present only when the result entity carries one |

## Pagination
- Default page size: 10, max: 50
- Use `start` + `count` to paginate. Check `hasMore` for more pages.

## Example workflows
1. **Market research**: Search by industry + location → map the competitive landscape
2. **Sales targeting**: Search by industry + size → build a list of target accounts
3. **Partnership discovery**: Search by keywords + location → find potential partners

## Credits


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

Find job listings on LinkedIn by keywords, location, job type, experience level, and workplace type. Returns lightweight job rows (title, company, companyUrl, companyLogo, location, workplaceType, postedAt, jobUrl, listingId). For RICH job-detail (applicant count, full description, employment status, listed/expire timestamps, inferred benefits, formattedJobFunctions, formattedIndustries, applyMethod, companyDescription), pass the result's `listingId` to `visitJob` (or POST `/api/visit/linkedin/job`).

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
Pass human-readable names for `location`, `company`, `industry`, `jobFunction`, `benefits`, `commitments` — they are resolved to LinkedIn IDs server-side. Do not hand-resolve.

| Filter | Type | Description |
|--------|------|-------------|
| `location` | string[] | City/region/country names |
| `company` | string[] | Hiring company names |
| `industry` | string[] | Company industry names |
| `jobFunction` | string[] | Job function names (Engineering, Sales, …) |
| `datePosted` | string | `"past-24h"` \| `"past-week"` \| `"past-month"` |
| `sortBy` | string | `"relevance"` \| `"date"` |
| `jobType` | string[] | Employment type codes (see below) |
| `experienceLevel` | string[] | Seniority codes (see below) |
| `workplaceType` | string[] | Work location codes (see below) |
| `benefits` | string[] | Advertised benefit names |
| `commitments` | string[] | Employer commitment names |
| `easyApply` | boolean | Only Easy Apply jobs |
| `under10Applicants` | boolean | Only jobs with <10 applicants |
| `inYourNetwork` | boolean | Only jobs where you have a connection |
| `hasVerifications` | boolean | Only verified job posters |
| `fairChanceEmployer` | boolean | Only Fair Chance employers |

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

## What is read from the URL
Keywords and every filter the vertical can actually apply, under LinkedIn's own spellings as its filter bar writes them (`titleFreeText`, `schoolFilter`, `companySizeV2`, `companyHQBingGeo`, `industryCompanyVertical`) with the bare names accepted as a fallback for a hand-written URL. A company's HEADQUARTERS is kept as its own filter and never folded into the person's location: they are different questions and return different people. Jobs facets are comma-separated in LinkedIn's URLs and each value is read on its own.

A facet the URL carries that this search cannot apply comes back as a `URL_FACET` entry in `warnings`, naming the facet. That matters because a dropped filter means the search ran WIDER than the one on the person's screen, so a result set with URL_FACET warnings is a bigger cohort than they asked for and should be described that way.

## Pagination override
You can optionally pass `start` and `count` to override the pagination embedded in the URL.

## Credits


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

## listSalesNavFilters

Returns the Sales Navigator filter panel — every filter you can use, grouped, with how to supply each value.

Call this ONCE at the start of a Sales Nav search task — like a human opening the filter panel. It tells you:
- which filters exist (seat tiers differ — Core / Advanced / Advanced Plus expose different filters);
- the BeReach `field` name to set on the search for each;
- the `valueKind` (enum / entity / toggle / range / text) so you know how to supply the value;
- `supportsExclude` and `available` (false = the seat tier does not have this filter — don't promise it to the user).

Requires an active Sales Nav seat.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSalesNavFilters" method="get" path="/search/linkedin/sales-nav/filters" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.listSalesNavFilters();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchListSalesNavFilters } from "bereach/funcs/search-list-sales-nav-filters.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchListSalesNavFilters(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchListSalesNavFilters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSalesNavFiltersResponse](../../models/operations/list-sales-nav-filters-response.md)\>**

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

## listSalesNavPersonas

Returns the user's custom buyer-persona library from Sales Navigator home (`sales.linkedin.com/home`).

Call this BEFORE setting the `persona` filter on a Sales Nav search. The agent has no way to guess persona ids — they are user-defined. Match the user's intent against the returned `name` + `criteriaSummary`.

Requires an active Sales Nav seat (403 otherwise — same gate as the search tools).

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSalesNavPersonas" method="get" path="/search/linkedin/sales-nav/personas" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.listSalesNavPersonas();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchListSalesNavPersonas } from "bereach/funcs/search-list-sales-nav-personas.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchListSalesNavPersonas(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchListSalesNavPersonas failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSalesNavPersonasResponse](../../models/operations/list-sales-nav-personas-response.md)\>**

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

## listSalesNavSavedSearches

Returns the user's saved Sales Navigator searches.

Call this at the start of a search task when the user references prior work ("run my fintech search", "the usual list"). Match the user's intent against the returned `name`, then pass the matching `savedSearchUrl` straight into `search_sales_nav_people` / `search_sales_nav_companies` via the `url` field — no filter assembly needed.

Requires an active Sales Nav seat.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSalesNavSavedSearches" method="get" path="/search/linkedin/sales-nav/saved-searches" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.listSalesNavSavedSearches();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchListSalesNavSavedSearches } from "bereach/funcs/search-list-sales-nav-saved-searches.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchListSalesNavSavedSearches(bereach);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchListSalesNavSavedSearches failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSalesNavSavedSearchesResponse](../../models/operations/list-sales-nav-saved-searches-response.md)\>**

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

## searchParameters

Resolve a written label (an industry, a company, a place, a school) into the identifier a search filter needs. Worth knowing why this exists: a filter given an id it does not recognise is accepted and ignored, so a search built on a guessed id quietly returns the unfiltered set and reads as a market with nobody in it. Leaving the keywords empty on a closed-value type lists every option, which is the way to answer what the available buckets are.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchParameters" method="get" path="/search/linkedin/parameters" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.searchParameters({
    type: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchSearchParameters } from "bereach/funcs/search-search-parameters.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchSearchParameters(bereach, {
    type: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchSearchParameters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SearchParametersRequest](../../models/operations/search-parameters-request.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SearchParametersResponse](../../models/operations/search-parameters-response.md)\>**

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

## resolveProfiles

Turn a mixed batch of LinkedIn identifiers into canonical profile URLs. Sales Navigator links and encrypted-id links cannot be stored or reliably matched against a contact; this is what upgrades them. Cached results cost nothing, and duplicates are removed before anything is spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resolveProfiles" method="post" path="/resolve/linkedin/profiles" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.resolveProfiles({
    inputs: [
      "<value 1>",
      "<value 2>",
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
import { searchResolveProfiles } from "bereach/funcs/search-resolve-profiles.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchResolveProfiles(bereach, {
    inputs: [
      "<value 1>",
      "<value 2>",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchResolveProfiles failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResolveProfilesRequest](../../models/operations/resolve-profiles-request.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ResolveProfilesResponse](../../models/operations/resolve-profiles-response.md)\>**

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
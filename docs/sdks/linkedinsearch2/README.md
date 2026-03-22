# LinkedinSearch

## Overview

### Available Operations

* [searchPosts](#searchposts) - Search LinkedIn Posts
* [searchPeople](#searchpeople) - Search LinkedIn People
* [searchJobs](#searchjobs) - Search LinkedIn Jobs
* [searchByUrl](#searchbyurl) - Search LinkedIn by URL

## searchPosts

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
  const result = await bereach.linkedinSearch.searchPosts({
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
import { linkedinSearchSearchPosts } from "bereach/funcs/linkedin-search-search-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinSearchSearchPosts(bereach, {
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
    console.log("linkedinSearchSearchPosts failed:", res.error);
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

## searchPeople

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
  const result = await bereach.linkedinSearch.searchPeople({
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
import { linkedinSearchSearchPeople } from "bereach/funcs/linkedin-search-search-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinSearchSearchPeople(bereach, {
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
    console.log("linkedinSearchSearchPeople failed:", res.error);
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

## searchJobs

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
  const result = await bereach.linkedinSearch.searchJobs({
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
import { linkedinSearchSearchJobs } from "bereach/funcs/linkedin-search-search-jobs.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinSearchSearchJobs(bereach, {
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
    console.log("linkedinSearchSearchJobs failed:", res.error);
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

## searchByUrl

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
  const result = await bereach.linkedinSearch.searchByUrl({
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
import { linkedinSearchSearchByUrl } from "bereach/funcs/linkedin-search-search-by-url.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinSearchSearchByUrl(bereach, {
    url: "https://www.linkedin.com/search/results/people/?keywords=software%20engineer&network=%5B%22S%22%5D&origin=FACETED_SEARCH",
    count: 10,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinSearchSearchByUrl failed:", res.error);
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
# SalesNav

## Overview

Search LinkedIn Sales Navigator for leads (people) and accounts (companies). Requires an active Sales Navigator subscription.

### Available Operations

* [searchPeople](#searchpeople) - Sales Navigator People/Lead Search

## searchPeople

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
| `profileUrl` | string | Public LinkedIn profile URL |
| `salesNavUrl` | string | Sales Navigator lead URL |
| `networkDistance` | string | Connection degree |
| `premium` | boolean | LinkedIn Premium subscriber |
| `openProfile` | boolean | Accepts free InMail |
| `pendingInvitation` | boolean | Connection request already sent |
| `currentPositions` | array | With company, role, tenure details |

## Credits
1 credit per 10 items returned.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="searchSalesNavPeople" method="post" path="/search/linkedin/sales-nav/people" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.salesNav.searchPeople({
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
import { salesNavSearchPeople } from "bereach/funcs/sales-nav-search-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await salesNavSearchPeople(bereach, {
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
    console.log("salesNavSearchPeople failed:", res.error);
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
# Public

## Overview

Public data: people, companies and posts from our search

### Available Operations

* [publicProfile](#publicprofile) - Read a public profile
* [publicFindPeople](#publicfindpeople) - Find people from public data
* [publicFindCompanies](#publicfindcompanies) - Find companies from public data
* [publicFindEmployees](#publicfindemployees) - Find the people at a company from public profiles
* [publicCompany](#publiccompany) - Read a public company page
* [publicFindPosts](#publicfindposts) - Find public posts by topic or by who posted
* [publicFindSignals](#publicfindsignals) - Find people to contact because something just happened at their company
* [publicEnrich](#publicenrich) - Enrich a list of contacts
* [planSearches](#plansearches) - Turn any material into a plan of searches
* [runSearches](#runsearches) - Run a plan of searches

## publicProfile

Read a professional profile, or up to 25 in one call, and save each as an enriched contact. One profile is read on preview and several in full, unless detail says otherwise. Preview gives the name, current employer, place, photo, follower count, the opening of the About and the latest posts, in about 3 seconds. Full gives the real headline, the current title with its start date, the dated career, schools, place and country, the About, languages and the connection and follower counts, usually live (readAt says when an older copy was used), in about 2 seconds a person. Your own profile is read in full and never saved. This is the default way to look up or enrich a person. Cost: 1 credit a person on preview and at most 1 credit a person on full; nothing for a person a search already returned or one not read. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicProfile" method="post" path="/public/profile" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicProfile({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicProfile } from "bereach/funcs/public-public-profile.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicProfile(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicProfile failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicProfileRequest](../../models/operations/public-profile-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicProfileResponse](../../models/operations/public-profile-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicFindPeople

Find people from public profiles: found profiles save as contacts and render as a people list you narrate with a one-line count. One ask is one call: every plausible title, seniority or city as an array on the SAME field, any headline signal in filters.keywords, limit (1-100, default 15) set by the number or volume word they used, sentence added when they named one person rather than a crowd, and more:true, excludeWords or excludeProfiles only to continue or refine a search that already ran. When companies to leave out or a company size are set, the answer says how many people it left out: say so. The people come from our index, about 3 weeks old at the median, so a recent job move can be missing; a search answers in about 2 seconds, and one in ten takes about 10 or more. Cost: each search costs by the results it brings back: 4 credits for up to 10, 11 for 25, 49 for 100; reading the profiles adds 1 credit for every 2, and a company size check 1 credit for every 2 companies; people already saved come at no cost. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicFindPeople" method="post" path="/public/search" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicFindPeople({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicFindPeople } from "bereach/funcs/public-public-find-people.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicFindPeople(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicFindPeople failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicFindPeopleRequest](../../models/operations/public-find-people-request.md)                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicFindPeopleResponse](../../models/operations/public-find-people-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicFindCompanies

Find companies from public data. Each row is the company's own identity: name, homepage, what it says it does, headcount, city, country and founding year. No people and no company page link come back. When a company size, a funding window or companies to leave out are set, the answer says how many companies it left out: say so. The companies come from our index, so a recent change to a company can be missing. Cost: each search costs by the results it brings back: 4 credits for up to 10, 11 for 25, 49 for 100; a company size check adds 1 credit for every 2 companies. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicFindCompanies" method="post" path="/public/companies" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicFindCompanies({
    filters: {},
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicFindCompanies } from "bereach/funcs/public-public-find-companies.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicFindCompanies(bereach, {
    filters: {},
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicFindCompanies failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicFindCompaniesRequest](../../models/operations/public-find-companies-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicFindCompaniesResponse](../../models/operations/public-find-companies-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicFindEmployees

The people who work at one named company now, from public profiles. Give the company by name or page address, and a role in keywords to narrow to whoever holds it. The people come from our index, about 3 weeks old at the median, so a recent job move can be missing. Cost: each search buys the smallest page that covers the count, 4 credits for up to 10, 11 for 25, 49 for 100, and another is bought only when the first did not find enough; more pays only for the searches not bought before; nothing when nobody comes back. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicFindEmployees" method="post" path="/public/employees" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicFindEmployees({
    company: "Davis and Sons",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicFindEmployees } from "bereach/funcs/public-public-find-employees.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicFindEmployees(bereach, {
    company: "Davis and Sons",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicFindEmployees failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicFindEmployeesRequest](../../models/operations/public-find-employees-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicFindEmployeesResponse](../../models/operations/public-find-employees-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicCompany

Read a public company page: identity, description, tagline, logo, follower and employee counts, website, head office, industry and founded year, recent posts, and the pages it shows beside it. Recent posts can be mined for people with collect_engagers. Up to date, with industry and founded year, in about 2 seconds, a few more when the company is named rather than given by its page address. Cost: 1 credit for the page and at most 4 more for its industry and founded year (nothing when they are already on file or not found), 4 more when the company is named rather than given by its page address; the same company again the same day is free. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicCompany" method="post" path="/public/company" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicCompany({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicCompany } from "bereach/funcs/public-public-company.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicCompany(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicCompany failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicCompanyRequest](../../models/operations/public-company-request.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicCompanyResponse](../../models/operations/public-company-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicFindPosts

Search public posts by topic or hashtag, by one person (author), by the people at a company (authorCompany), or by a kind of person (authorTitle, authorLocation). Each post carries who published it and when, and can be mined for people with collect_engagers. The people who wrote the posts are saved to the list unless save is skip. Cost: posts by one person cost one search by the posts it brings back: 4 credits for up to 10, 11 for 25, 24 for 50; any other post search costs by the posts it asks for and the authors it checks: 9 credits for up to 10 posts, 24 for 25, 49 for 50 (19 for 10 when a company or a place is checked), plus about 1 credit for every 2 authors checked; nothing when no post comes back; reading the posts in full adds 1 credit a page of results. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicFindPosts" method="post" path="/public/post-search" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicFindPosts({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicFindPosts } from "bereach/funcs/public-public-find-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicFindPosts(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicFindPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicFindPostsRequest](../../models/operations/public-find-posts-request.md)                                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicFindPostsResponse](../../models/operations/public-find-posts-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicFindSignals

Two steps from public data. mode events returns dated events (a raise, an appointment, a job opening) for a description of the event, each with its title, date, source page and an id. mode resolve takes companies read in those events, each with a role to reach or the person the event names, and returns the company's LinkedIn page and the people found, each with their profile and the event. A company whose page is not found returns nobody. Events and people already returned never come back; an events ask with includeText keeps its own record, so it can return an event a wider ask already gave. The people found are saved to the list unless save is skip. Each event carries its date; the people come from our index, about 3 weeks old at the median, so a recent job move can be missing. Cost: each search costs by the results it brings back: 4 credits for up to 10, 11 for 25, 49 for 100; in mode resolve, each company costs its searches plus 1 credit for every 2 profiles read, and nothing when nobody comes back. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicFindSignals" method="post" path="/public/signals" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicFindSignals({
    mode: "events",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPublicFindSignals } from "bereach/funcs/public-public-find-signals.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicFindSignals(bereach, {
    mode: "events",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicFindSignals failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicFindSignalsRequest](../../models/operations/public-find-signals-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicFindSignalsResponse](../../models/operations/public-find-signals-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## publicEnrich

Enrich many of your own saved contacts in one call, by contact id from a list already shown, never a raw profile URL and never one public_profile per person: On full (the default) each person gets the fullest record we can read: the real headline, the current title with its start date, the dated career, schools, place and country, the About and languages, usually live, in about 2 seconds a person, in the background; preview gives only the basics: name, employer, place and photo. Not for email or phone; ask which people when the target is ambiguous rather than defaulting to everyone. Cost: at most 1 credit a person, nothing for a person a search already returned or one not read; degree details add nothing. creditsUsed says what the call spent.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="publicEnrich" method="post" path="/public/enrich" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.publicEnrich({
    contactIds: [
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
import { publicPublicEnrich } from "bereach/funcs/public-public-enrich.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPublicEnrich(bereach, {
    contactIds: [
      "<value 1>",
      "<value 2>",
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPublicEnrich failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PublicEnrichRequest](../../models/operations/public-enrich-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PublicEnrichResponse](../../models/operations/public-enrich-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## planSearches

Read what someone sells and who they want to reach, from their own words, the text of documents or pages, or page addresses read by the server, and answer with a plan of people searches: what was said and what was inferred, the segments with their kinds of company, places and job titles, the searches a run would send and what they cost. While something blocking is missing the answer carries up to five questions and no searches; call again with plan_id and the answers. Free: nothing is searched, charged or saved. In a conversation the plan is that conversation's own, and a later call changes it.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="planSearches" method="post" path="/public/plan-searches" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.planSearches({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicPlanSearches } from "bereach/funcs/public-plan-searches.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicPlanSearches(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicPlanSearches failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PlanSearchesRequest](../../models/operations/plan-searches-request.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PlanSearchesResponse](../../models/operations/plan-searches-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |

## runSearches

Run a ready plan returned by plan-searches, in the background, and save the people it finds into the conversation's list, or your contacts outside one. Answers within about 25 seconds with a receipt: people added so far, credits used, and each search's state. A run answers in about 6 seconds, and one in ten takes about 10 or more; the people come from our index, about 3 weeks old at the median, so a recent job move can be missing. A plan runs once: calling again with the same plan_id answers where its run stands and spends nothing more. Every search is charged to the workspace credit pool like a people search, and the run never spends more than the plan's cost_estimate_credits.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="runSearches" method="post" path="/public/run-searches" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.public.runSearches({
    planId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { publicRunSearches } from "bereach/funcs/public-run-searches.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await publicRunSearches(bereach, {
    planId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("publicRunSearches failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.RunSearchesRequest](../../models/operations/run-searches-request.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.RunSearchesResponse](../../models/operations/run-searches-response.md)\>**

### Errors

| Error Type                                   | Status Code                                  | Content Type                                 |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| errors.ResponseBodyBadRequestError1          | 400                                          | application/json                             |
| errors.ResponseBodyBadRequestError2          | 400                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError1        | 401                                          | application/json                             |
| errors.ResponseBodyUnauthorizedError2        | 401                                          | application/json                             |
| errors.ResponseBodyForbiddenError1           | 403                                          | application/json                             |
| errors.ResponseBodyForbiddenError2           | 403                                          | application/json                             |
| errors.ResponseBodyNotFoundError1            | 404                                          | application/json                             |
| errors.ResponseBodyNotFoundError2            | 404                                          | application/json                             |
| errors.ResponseBodyConflictError1            | 409                                          | application/json                             |
| errors.ResponseBodyConflictError2            | 409                                          | application/json                             |
| errors.ResponseBodyGoneError1                | 410                                          | application/json                             |
| errors.ResponseBodyGoneError2                | 410                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError1 | 422                                          | application/json                             |
| errors.ResponseBodyUnprocessableEntityError2 | 422                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError1     | 429                                          | application/json                             |
| errors.ResponseBodyTooManyRequestsError2     | 429                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError1 | 500                                          | application/json                             |
| errors.ResponseBodyInternalServerErrorError2 | 500                                          | application/json                             |
| errors.ResponseBodyBadGatewayError1          | 502                                          | application/json                             |
| errors.ResponseBodyBadGatewayError2          | 502                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError1  | 503                                          | application/json                             |
| errors.ResponseBodyServiceUnavailableError2  | 503                                          | application/json                             |
| errors.BereachDefaultError                   | 4XX, 5XX                                     | \*/\*                                        |
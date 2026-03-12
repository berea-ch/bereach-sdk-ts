# Scrapers

## Overview

### Available Operations

* [collectPosts](#collectposts) - Scrape LinkedIn profile posts
* [visitProfile](#visitprofile) - Visit LinkedIn profile and extract contact data

## collectPosts

Authenticates the requester, validates LinkedIn credentials, and returns paginated posts from a LinkedIn profile. Supports count, start, and paginationToken for pagination.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="collectLinkedInPosts" method="post" path="/collect/linkedin/posts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.scrapers.collectPosts({
    profileUrl: "https://www.linkedin.com/in/username",
    count: 20,
    start: 0,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { scrapersCollectPosts } from "bereach/funcs/scrapers-collect-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await scrapersCollectPosts(bereach, {
    profileUrl: "https://www.linkedin.com/in/username",
    count: 20,
    start: 0,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scrapersCollectPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectLinkedInPostsRequest](../../models/operations/collect-linked-in-posts-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectLinkedInPostsResponse](../../models/operations/collect-linked-in-posts-response.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.CollectLinkedInPostsBadRequestError          | 400                                                 | application/json                                    |
| errors.CollectLinkedInPostsUnauthorizedError        | 401                                                 | application/json                                    |
| errors.CollectLinkedInPostsForbiddenError           | 403                                                 | application/json                                    |
| errors.CollectLinkedInPostsNotFoundError            | 404                                                 | application/json                                    |
| errors.CollectLinkedInPostsConflictError            | 409                                                 | application/json                                    |
| errors.CollectLinkedInPostsGoneError                | 410                                                 | application/json                                    |
| errors.CollectLinkedInPostsUnprocessableEntityError | 422                                                 | application/json                                    |
| errors.CollectLinkedInPostsTooManyRequestsError     | 429                                                 | application/json                                    |
| errors.CollectLinkedInPostsInternalServerError      | 500                                                 | application/json                                    |
| errors.BereachDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |

## visitProfile

Visit a LinkedIn profile and return contact data. Distance-1 profiles cached 24h. No dedup — always executes. campaignSlug is for tracking only.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="visitLinkedInProfile" method="post" path="/visit/linkedin/profile" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.scrapers.visitProfile({
    profile: "https://www.linkedin.com/in/alexandre-sarfati",
    campaignSlug: "lead-magnet-post-12345",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { scrapersVisitProfile } from "bereach/funcs/scrapers-visit-profile.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await scrapersVisitProfile(bereach, {
    profile: "https://www.linkedin.com/in/alexandre-sarfati",
    campaignSlug: "lead-magnet-post-12345",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("scrapersVisitProfile failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.VisitLinkedInProfileRequest](../../models/operations/visit-linked-in-profile-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.VisitLinkedInProfileResponse](../../models/operations/visit-linked-in-profile-response.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.VisitLinkedInProfileBadRequestError          | 400                                                 | application/json                                    |
| errors.VisitLinkedInProfileUnauthorizedError        | 401                                                 | application/json                                    |
| errors.VisitLinkedInProfileForbiddenError           | 403                                                 | application/json                                    |
| errors.VisitLinkedInProfileNotFoundError            | 404                                                 | application/json                                    |
| errors.VisitLinkedInProfileConflictError            | 409                                                 | application/json                                    |
| errors.VisitLinkedInProfileGoneError                | 410                                                 | application/json                                    |
| errors.VisitLinkedInProfileUnprocessableEntityError | 422                                                 | application/json                                    |
| errors.VisitLinkedInProfileTooManyRequestsError     | 429                                                 | application/json                                    |
| errors.VisitLinkedInProfileInternalServerError      | 500                                                 | application/json                                    |
| errors.BereachDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |
# LinkedinScrapers

## Overview

### Available Operations

* [collectLikes](#collectlikes) - Scrape LinkedIn post likes
* [collectComments](#collectcomments) - Scrape LinkedIn post comments
* [visitCompany](#visitcompany) - Visit LinkedIn company page and extract profile data
* [listSavedPosts](#listsavedposts) - List saved posts
* [collectHashtagPosts](#collecthashtagposts) - Collect posts from a hashtag

## collectLikes

Authenticates the requester, validates LinkedIn credentials, and returns up to 100 profiles per page that reacted to the specified post (LinkedIn API limit). Supports pagination.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="collectLinkedInLikes" method="post" path="/collect/linkedin/likes" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl: "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
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
import { linkedinScrapersCollectLikes } from "bereach/funcs/linkedin-scrapers-collect-likes.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinScrapersCollectLikes(bereach, {
    postUrl: "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinScrapersCollectLikes failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectLinkedInLikesRequest](../../models/operations/collect-linked-in-likes-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectLinkedInLikesResponse](../../models/operations/collect-linked-in-likes-response.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.CollectLinkedInLikesBadRequestError          | 400                                                 | application/json                                    |
| errors.CollectLinkedInLikesUnauthorizedError        | 401                                                 | application/json                                    |
| errors.CollectLinkedInLikesForbiddenError           | 403                                                 | application/json                                    |
| errors.CollectLinkedInLikesNotFoundError            | 404                                                 | application/json                                    |
| errors.CollectLinkedInLikesConflictError            | 409                                                 | application/json                                    |
| errors.CollectLinkedInLikesGoneError                | 410                                                 | application/json                                    |
| errors.CollectLinkedInLikesUnprocessableEntityError | 422                                                 | application/json                                    |
| errors.CollectLinkedInLikesTooManyRequestsError     | 429                                                 | application/json                                    |
| errors.CollectLinkedInLikesInternalServerError      | 500                                                 | application/json                                    |
| errors.BereachDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |

## collectComments

Returns paginated top-level comments for a LinkedIn post (newest first). Use count=0 for a free total-only check (0 credits, no rate-limit slot consumed). Response includes previousTotal (server-cached) to detect new comments without client tracking.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="collectLinkedInComments" method="post" path="/collect/linkedin/comments" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectComments({
    postUrl: "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
    count: 100,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinScrapersCollectComments } from "bereach/funcs/linkedin-scrapers-collect-comments.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinScrapersCollectComments(bereach, {
    postUrl: "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
    count: 100,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinScrapersCollectComments failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectLinkedInCommentsRequest](../../models/operations/collect-linked-in-comments-request.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectLinkedInCommentsResponse](../../models/operations/collect-linked-in-comments-response.md)\>**

### Errors

| Error Type                                             | Status Code                                            | Content Type                                           |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| errors.CollectLinkedInCommentsBadRequestError          | 400                                                    | application/json                                       |
| errors.CollectLinkedInCommentsUnauthorizedError        | 401                                                    | application/json                                       |
| errors.CollectLinkedInCommentsForbiddenError           | 403                                                    | application/json                                       |
| errors.CollectLinkedInCommentsNotFoundError            | 404                                                    | application/json                                       |
| errors.CollectLinkedInCommentsConflictError            | 409                                                    | application/json                                       |
| errors.CollectLinkedInCommentsGoneError                | 410                                                    | application/json                                       |
| errors.CollectLinkedInCommentsUnprocessableEntityError | 422                                                    | application/json                                       |
| errors.CollectLinkedInCommentsTooManyRequestsError     | 429                                                    | application/json                                       |
| errors.CollectLinkedInCommentsInternalServerError      | 500                                                    | application/json                                       |
| errors.BereachDefaultError                             | 4XX, 5XX                                               | \*/\*                                                  |

## visitCompany

Fetches a LinkedIn company profile by URL or universal name. Returns structured company data including description, industry, employee count, headquarters, logo, affiliated/similar companies, and more. Optionally enriches with workplace policy data (costs 1 extra credit per optional API call). Base cost: 1 credit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="visitLinkedInCompany" method="post" path="/visit/linkedin/company" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.visitCompany({
    companyUrl: "https://www.linkedin.com/company/openai",
    includeWorkplacePolicy: true,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinScrapersVisitCompany } from "bereach/funcs/linkedin-scrapers-visit-company.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinScrapersVisitCompany(bereach, {
    companyUrl: "https://www.linkedin.com/company/openai",
    includeWorkplacePolicy: true,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinScrapersVisitCompany failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.VisitLinkedInCompanyRequest](../../models/operations/visit-linked-in-company-request.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.VisitLinkedInCompanyResponse](../../models/operations/visit-linked-in-company-response.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.VisitLinkedInCompanyBadRequestError          | 400                                                 | application/json                                    |
| errors.VisitLinkedInCompanyUnauthorizedError        | 401                                                 | application/json                                    |
| errors.VisitLinkedInCompanyForbiddenError           | 403                                                 | application/json                                    |
| errors.VisitLinkedInCompanyNotFoundError            | 404                                                 | application/json                                    |
| errors.VisitLinkedInCompanyConflictError            | 409                                                 | application/json                                    |
| errors.VisitLinkedInCompanyGoneError                | 410                                                 | application/json                                    |
| errors.VisitLinkedInCompanyUnprocessableEntityError | 422                                                 | application/json                                    |
| errors.VisitLinkedInCompanyTooManyRequestsError     | 429                                                 | application/json                                    |
| errors.VisitLinkedInCompanyInternalServerError      | 500                                                 | application/json                                    |
| errors.BereachDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |

## listSavedPosts

List posts saved to bookmarks. 1 credit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="collectSavedLinkedInPosts" method="post" path="/collect/linkedin/saved" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.listSavedPosts({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinScrapersListSavedPosts } from "bereach/funcs/linkedin-scrapers-list-saved-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinScrapersListSavedPosts(bereach, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinScrapersListSavedPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectSavedLinkedInPostsRequest](../../models/operations/collect-saved-linked-in-posts-request.md)                                                                | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectSavedLinkedInPostsResponse](../../models/operations/collect-saved-linked-in-posts-response.md)\>**

### Errors

| Error Type                                               | Status Code                                              | Content Type                                             |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| errors.CollectSavedLinkedInPostsBadRequestError          | 400                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsUnauthorizedError        | 401                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsForbiddenError           | 403                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsNotFoundError            | 404                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsConflictError            | 409                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsGoneError                | 410                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsUnprocessableEntityError | 422                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsTooManyRequestsError     | 429                                                      | application/json                                         |
| errors.CollectSavedLinkedInPostsInternalServerError      | 500                                                      | application/json                                         |
| errors.BereachDefaultError                               | 4XX, 5XX                                                 | \*/\*                                                    |

## collectHashtagPosts

Collect posts from a LinkedIn hashtag feed. Pass hashtag name without # prefix. Supports pagination with start/count. Returns parsed post objects. 1 credit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="collectLinkedInHashtagPosts" method="post" path="/collect/linkedin/hashtag" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectHashtagPosts({
    hashtag: "AI",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { linkedinScrapersCollectHashtagPosts } from "bereach/funcs/linkedin-scrapers-collect-hashtag-posts.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await linkedinScrapersCollectHashtagPosts(bereach, {
    hashtag: "AI",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("linkedinScrapersCollectHashtagPosts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CollectLinkedInHashtagPostsRequest](../../models/operations/collect-linked-in-hashtag-posts-request.md)                                                            | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.CollectLinkedInHashtagPostsResponse](../../models/operations/collect-linked-in-hashtag-posts-response.md)\>**

### Errors

| Error Type                                                 | Status Code                                                | Content Type                                               |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| errors.CollectLinkedInHashtagPostsBadRequestError          | 400                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsUnauthorizedError        | 401                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsForbiddenError           | 403                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsNotFoundError            | 404                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsConflictError            | 409                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsGoneError                | 410                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsUnprocessableEntityError | 422                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsTooManyRequestsError     | 429                                                        | application/json                                           |
| errors.CollectLinkedInHashtagPostsInternalServerError      | 500                                                        | application/json                                           |
| errors.BereachDefaultError                                 | 4XX, 5XX                                                   | \*/\*                                                      |
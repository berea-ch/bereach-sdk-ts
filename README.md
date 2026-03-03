# bereach

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *bereach* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=bereach&utm_campaign=typescript)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)

<!-- Start Summary [summary] -->
## Summary

BeReach API: BeReach | Unofficial Linkedin API
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [bereach](#bereach)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add bereach
```

### PNPM

```bash
pnpm add bereach
```

### Bun

```bash
bun add bereach
```

### Yarn

```bash
yarn add bereach
```

> [!NOTE]
> This package is published as an ES Module (ESM) only. For applications using
> CommonJS, use `await import("bereach")` to import and use this package.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](https://github.com/berea-ch/bereach-sdk-ts/blob/main/RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl:
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name    | Type | Scheme      | Environment Variable |
| ------- | ---- | ----------- | -------------------- |
| `token` | http | HTTP Bearer | `BEREACH_TOKEN`      |

To authenticate with the API the `token` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl:
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  });

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [Campaigns](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md)

* [~~filter~~](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#filter) - Check if campaign actions are completed :warning: **Deprecated**
* [getStatus](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#getstatus) - Query per-profile action status within a campaign
* [syncActions](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#syncactions) - Mark actions as completed without performing them
* [getStats](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#getstats) - Get aggregate campaign statistics

### [LinkedinActions](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md)

* [connectProfile](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#connectprofile) - Send LinkedIn connection request
* [listInvitations](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#listinvitations) - List received LinkedIn connection invitations
* [acceptInvitation](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
* [sendMessage](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#sendmessage) - Send LinkedIn message
* [replyToComment](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#replytocomment) - Reply to a LinkedIn comment
* [likeComment](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#likecomment) - Like a LinkedIn comment
* [publishPost](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#publishpost) - Publish or schedule a LinkedIn post

### [LinkedinChat](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md)

* [listConversations](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#listconversations) - List LinkedIn inbox conversations
* [searchConversations](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#searchconversations) - Search LinkedIn conversations
* [findConversation](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#findconversation) - Find a conversation with a specific person
* [getMessages](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#getmessages) - Read messages from a conversation

### [LinkedinScrapers](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md)

* [collectLikes](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectlikes) - Scrape LinkedIn post likes
* [collectComments](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectcomments) - Scrape LinkedIn post comments
* [collectCommentReplies](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectcommentreplies) - Scrape replies to a LinkedIn comment
* [collectPosts](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectposts) - Scrape LinkedIn profile posts
* [visitProfile](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
* [visitCompany](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#visitcompany) - Visit LinkedIn company page and extract profile data

### [LinkedinSearch](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md)

* [unifiedSearch](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#unifiedsearch) - Unified LinkedIn Search — posts, people, companies, jobs
* [searchPosts](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchposts) - Search LinkedIn Posts
* [searchPeople](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchpeople) - Search LinkedIn People
* [searchCompanies](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchcompanies) - Search LinkedIn Companies
* [searchJobs](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchjobs) - Search LinkedIn Jobs
* [searchByUrl](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchbyurl) - Search LinkedIn by URL
* [resolveParameters](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)

### [Profile](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md)

* [getLinkedInProfile](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getlinkedinprofile) - Get authenticated user's LinkedIn profile
* [refresh](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#refresh) - Refresh authenticated user's LinkedIn profile
* [getPosts](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getposts) - Get authenticated user's LinkedIn posts
* [getFollowers](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
* [getLimits](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getlimits) - Get current LinkedIn rate limit status
* [getCredits](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](https://github.com/berea-ch/bereach-sdk-ts/blob/main/FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`campaignsGetStats`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#getstats) - Get aggregate campaign statistics
- [`campaignsGetStatus`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#getstatus) - Query per-profile action status within a campaign
- [`campaignsSyncActions`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#syncactions) - Mark actions as completed without performing them
- [`linkedinActionsAcceptInvitation`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
- [`linkedinActionsConnectProfile`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#connectprofile) - Send LinkedIn connection request
- [`linkedinActionsLikeComment`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#likecomment) - Like a LinkedIn comment
- [`linkedinActionsListInvitations`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#listinvitations) - List received LinkedIn connection invitations
- [`linkedinActionsPublishPost`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#publishpost) - Publish or schedule a LinkedIn post
- [`linkedinActionsReplyToComment`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#replytocomment) - Reply to a LinkedIn comment
- [`linkedinActionsSendMessage`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinactions/README.md#sendmessage) - Send LinkedIn message
- [`linkedinChatFindConversation`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#findconversation) - Find a conversation with a specific person
- [`linkedinChatGetMessages`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#getmessages) - Read messages from a conversation
- [`linkedinChatListConversations`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#listconversations) - List LinkedIn inbox conversations
- [`linkedinChatSearchConversations`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinchat/README.md#searchconversations) - Search LinkedIn conversations
- [`linkedinScrapersCollectCommentReplies`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectcommentreplies) - Scrape replies to a LinkedIn comment
- [`linkedinScrapersCollectComments`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectcomments) - Scrape LinkedIn post comments
- [`linkedinScrapersCollectLikes`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectlikes) - Scrape LinkedIn post likes
- [`linkedinScrapersCollectPosts`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#collectposts) - Scrape LinkedIn profile posts
- [`linkedinScrapersVisitCompany`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#visitcompany) - Visit LinkedIn company page and extract profile data
- [`linkedinScrapersVisitProfile`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinscrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
- [`linkedinSearchResolveParameters`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)
- [`linkedinSearchSearchByUrl`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchbyurl) - Search LinkedIn by URL
- [`linkedinSearchSearchCompanies`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchcompanies) - Search LinkedIn Companies
- [`linkedinSearchSearchJobs`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchjobs) - Search LinkedIn Jobs
- [`linkedinSearchSearchPeople`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchpeople) - Search LinkedIn People
- [`linkedinSearchSearchPosts`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#searchposts) - Search LinkedIn Posts
- [`linkedinSearchUnifiedSearch`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/linkedinsearch/README.md#unifiedsearch) - Unified LinkedIn Search — posts, people, companies, jobs
- [`profileGetCredits`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance
- [`profileGetFollowers`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
- [`profileGetLimits`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getlimits) - Get current LinkedIn rate limit status
- [`profileGetLinkedInProfile`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getlinkedinprofile) - Get authenticated user's LinkedIn profile
- [`profileGetPosts`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#getposts) - Get authenticated user's LinkedIn posts
- [`profileRefresh`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/profile/README.md#refresh) - Refresh authenticated user's LinkedIn profile
- ~~[`campaignsFilter`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/docs/sdks/campaigns/README.md#filter)~~ - Check if campaign actions are completed :warning: **Deprecated**

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl:
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl:
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  });

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`BereachError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/bereach-error.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Bereach } from "bereach";
import * as errors from "bereach/models/errors";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  try {
    const result = await bereach.linkedinScrapers.collectLikes({
      postUrl:
        "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
      start: 0,
    });

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.BereachError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.BadRequestError) {
        console.log(error.data$.success); // boolean
        console.log(error.data$.error); // operations.CollectLinkedInLikesBadRequestError
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`BereachError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/bereach-error.ts): The base class for HTTP error responses.
  * [`BadRequestError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`.
  * [`UnauthorizedError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`.
  * [`ForbiddenError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/forbidden-error.ts): The client does not have access rights to the content. Status code `403`.
  * [`NotFoundError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/not-found-error.ts): The server cannot find the requested resource. Status code `404`.
  * [`ConflictError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/conflict-error.ts): The request conflicts with the current state of the server. Status code `409`.
  * [`GoneError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`.
  * [`UnprocessableEntityError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`.
  * [`TooManyRequestsError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`.
  * [`InternalServerError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/http-client-errors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/http-client-errors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/http-client-errors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/http-client-errors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/http-client-errors.ts): Unrecognised or unexpected error.


**Inherit from [`BereachError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/bereach-error.ts)**:
* [`ResponseValidationError`](https://github.com/berea-ch/bereach-sdk-ts/blob/main/src/models/errors/response-validation-error.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  serverURL: "https://api.berea.ch",
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.linkedinScrapers.collectLikes({
    postUrl:
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    start: 0,
  });

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to:
- route requests through a proxy server using [undici](https://www.npmjs.com/package/undici)'s ProxyAgent
- use the `"beforeRequest"` hook to add a custom header and a timeout to requests
- use the `"requestError"` hook to log errors

```typescript
import { Bereach } from "bereach";
import { ProxyAgent } from "undici";
import { HTTPClient } from "bereach/lib/http";

const dispatcher = new ProxyAgent("http://proxy.example.com:8080");

const httpClient = new HTTPClient({
  // 'fetcher' takes a function that has the same signature as native 'fetch'.
  fetcher: (input, init) =>
    // 'dispatcher' is specific to undici and not part of the standard Fetch API.
    fetch(input, { ...init, dispatcher } as RequestInit),
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Bereach({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Bereach } from "bereach";

const sdk = new Bereach({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `BEREACH_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=bereach&utm_campaign=typescript)

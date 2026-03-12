# bereach

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *bereach* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=bereach&utm_campaign=typescript)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/bereach-h29/bereach). Delete this section before > publishing to a package manager.

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

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
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

### [Actions](docs/sdks/actions/README.md)

* [connectProfile](docs/sdks/actions/README.md#connectprofile) - Send LinkedIn connection request
* [sendMessage](docs/sdks/actions/README.md#sendmessage) - Send LinkedIn message
* [listSentInvitations](docs/sdks/actions/README.md#listsentinvitations) - List sent connection invitations
* [followCompany](docs/sdks/actions/README.md#followcompany) - Follow a company

### [Campaigns](docs/sdks/campaigns/README.md)

* [~~filter~~](docs/sdks/campaigns/README.md#filter) - Check if campaign actions are completed :warning: **Deprecated**
* [getStatus](docs/sdks/campaigns/README.md#getstatus) - Query per-profile action status within a campaign
* [sync](docs/sdks/campaigns/README.md#sync) - Mark actions as completed without performing them
* [getStats](docs/sdks/campaigns/README.md#getstats) - Get aggregate campaign statistics

### [Chat](docs/sdks/chat/README.md)

* [searchConversations](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
* [findConversation](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
* [archive](docs/sdks/chat/README.md#archive) - Archive a conversation
* [unreact](docs/sdks/chat/README.md#unreact) - Remove emoji reaction from a message

### [CompanyPages](docs/sdks/companypages/README.md)

* [list](docs/sdks/companypages/README.md#list) - List company pages the user administers
* [getPosts](docs/sdks/companypages/README.md#getposts) - Get recent posts from a company page
* [getPermissions](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
* [getAnalytics](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics

### [Contacts](docs/sdks/contacts/README.md)

* [upsert](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)

### [LinkedinActions](docs/sdks/linkedinactions1/README.md)

* [listInvitations](docs/sdks/linkedinactions1/README.md#listinvitations) - List received LinkedIn connection invitations
* [acceptInvitation](docs/sdks/linkedinactions1/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
* [replyToComment](docs/sdks/linkedinactions1/README.md#replytocomment) - Reply to a LinkedIn comment
* [likePost](docs/sdks/linkedinactions1/README.md#likepost) - Like a LinkedIn post
* [withdrawInvitation](docs/sdks/linkedinactions1/README.md#withdrawinvitation) - Withdraw a sent connection invitation
* [followProfile](docs/sdks/linkedinactions1/README.md#followprofile) - Follow a profile
* [editPost](docs/sdks/linkedinactions1/README.md#editpost) - Edit a post
* [editComment](docs/sdks/linkedinactions1/README.md#editcomment) - Edit a comment
* [repostPost](docs/sdks/linkedinactions1/README.md#repostpost) - Repost / share a post
* [unlikePost](docs/sdks/linkedinactions1/README.md#unlikepost) - Unlike a post
* [unlikeComment](docs/sdks/linkedinactions1/README.md#unlikecomment) - Unlike a comment
* [unsavePost](docs/sdks/linkedinactions1/README.md#unsavepost) - Unsave a post
* [unfollowCompany](docs/sdks/linkedinactions1/README.md#unfollowcompany) - Unfollow a company

### [LinkedInActions](docs/sdks/linkedinactions2/README.md)

* [likeComment](docs/sdks/linkedinactions2/README.md#likecomment) - Like a LinkedIn comment
* [publishPost](docs/sdks/linkedinactions2/README.md#publishpost) - Publish or schedule a LinkedIn post
* [createComment](docs/sdks/linkedinactions2/README.md#createcomment) - Comment on a LinkedIn post
* [declineInvitation](docs/sdks/linkedinactions2/README.md#declineinvitation) - Decline a connection invitation
* [unfollowProfile](docs/sdks/linkedinactions2/README.md#unfollowprofile) - Unfollow a profile
* [savePost](docs/sdks/linkedinactions2/README.md#savepost) - Save a post

### [LinkedinChat](docs/sdks/linkedinchat1/README.md)

* [listInboxConversations](docs/sdks/linkedinchat1/README.md#listinboxconversations) - List LinkedIn inbox conversations
* [getMessages](docs/sdks/linkedinchat1/README.md#getmessages) - Read messages from a conversation
* [markAllRead](docs/sdks/linkedinchat1/README.md#markallread) - Mark all conversations as read
* [listArchived](docs/sdks/linkedinchat1/README.md#listarchived) - List archived conversations
* [react](docs/sdks/linkedinchat1/README.md#react) - React to a message with emoji
* [sendTypingIndicator](docs/sdks/linkedinchat1/README.md#sendtypingindicator) - Send typing indicator
* [getUnreadCount](docs/sdks/linkedinchat1/README.md#getunreadcount) - Get unread message count

### [LinkedInChat](docs/sdks/linkedinchat2/README.md)

* [markSeen](docs/sdks/linkedinchat2/README.md#markseen) - Mark a conversation as read
* [star](docs/sdks/linkedinchat2/README.md#star) - Star a conversation
* [unstar](docs/sdks/linkedinchat2/README.md#unstar) - Unstar a conversation
* [listStarred](docs/sdks/linkedinchat2/README.md#liststarred) - List starred conversations
* [unarchive](docs/sdks/linkedinchat2/README.md#unarchive) - Unarchive a conversation

### [LinkedinScrapers](docs/sdks/linkedinscrapers1/README.md)

* [collectLikes](docs/sdks/linkedinscrapers1/README.md#collectlikes) - Scrape LinkedIn post likes
* [collectComments](docs/sdks/linkedinscrapers1/README.md#collectcomments) - Scrape LinkedIn post comments
* [visitCompany](docs/sdks/linkedinscrapers1/README.md#visitcompany) - Visit LinkedIn company page and extract profile data
* [listSavedPosts](docs/sdks/linkedinscrapers1/README.md#listsavedposts) - List saved posts
* [collectHashtagPosts](docs/sdks/linkedinscrapers1/README.md#collecthashtagposts) - Collect posts from a hashtag

### [LinkedInScrapers](docs/sdks/linkedinscrapers2/README.md)

* [collectCommentReplies](docs/sdks/linkedinscrapers2/README.md#collectcommentreplies) - Scrape replies to a LinkedIn comment
* [getFeed](docs/sdks/linkedinscrapers2/README.md#getfeed) - Get home feed

### [LinkedinSearch](docs/sdks/linkedinsearch2/README.md)

* [searchPosts](docs/sdks/linkedinsearch2/README.md#searchposts) - Search LinkedIn Posts
* [searchPeople](docs/sdks/linkedinsearch2/README.md#searchpeople) - Search LinkedIn People
* [searchJobs](docs/sdks/linkedinsearch2/README.md#searchjobs) - Search LinkedIn Jobs
* [searchByUrl](docs/sdks/linkedinsearch2/README.md#searchbyurl) - Search LinkedIn by URL

### [LinkedInSearch](docs/sdks/linkedinsearch1/README.md)

* [search](docs/sdks/linkedinsearch1/README.md#search) - Unified LinkedIn Search — posts, people, companies, jobs
* [searchCompanies](docs/sdks/linkedinsearch1/README.md#searchcompanies) - Search LinkedIn Companies
* [resolveParameters](docs/sdks/linkedinsearch1/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)

### [Profile](docs/sdks/profile/README.md)

* [get](docs/sdks/profile/README.md#get) - Get authenticated user's LinkedIn profile
* [listAccounts](docs/sdks/profile/README.md#listaccounts) - List all LinkedIn accounts for the authenticated user
* [updateAccount](docs/sdks/profile/README.md#updateaccount) - Update a LinkedIn account (label, default)
* [refresh](docs/sdks/profile/README.md#refresh) - Refresh authenticated user's LinkedIn profile
* [getPosts](docs/sdks/profile/README.md#getposts) - Get authenticated user's LinkedIn posts
* [getFollowers](docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
* [getLimits](docs/sdks/profile/README.md#getlimits) - Get current LinkedIn rate limit status
* [getCredits](docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance
* [getProfileViews](docs/sdks/profile/README.md#getprofileviews) - Get profile views
* [getSearchAppearances](docs/sdks/profile/README.md#getsearchappearances) - Get search appearances
* [getPostAnalytics](docs/sdks/profile/README.md#getpostanalytics) - Get post analytics
* [getFollowerAnalytics](docs/sdks/profile/README.md#getfolloweranalytics) - Get follower analytics

### [SalesNav](docs/sdks/salesnav/README.md)

* [searchPeople](docs/sdks/salesnav/README.md#searchpeople) - Sales Navigator People/Lead Search

### [SalesNavigatorSearch](docs/sdks/salesnavigatorsearch/README.md)

* [search](docs/sdks/salesnavigatorsearch/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
* [searchCompanies](docs/sdks/salesnavigatorsearch/README.md#searchcompanies) - Sales Navigator Company/Account Search

### [Scrapers](docs/sdks/scrapers/README.md)

* [collectPosts](docs/sdks/scrapers/README.md#collectposts) - Scrape LinkedIn profile posts
* [visitProfile](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`actionsConnectProfile`](docs/sdks/actions/README.md#connectprofile) - Send LinkedIn connection request
- [`actionsFollowCompany`](docs/sdks/actions/README.md#followcompany) - Follow a company
- [`actionsListSentInvitations`](docs/sdks/actions/README.md#listsentinvitations) - List sent connection invitations
- [`actionsSendMessage`](docs/sdks/actions/README.md#sendmessage) - Send LinkedIn message
- [`campaignsGetStats`](docs/sdks/campaigns/README.md#getstats) - Get aggregate campaign statistics
- [`campaignsGetStatus`](docs/sdks/campaigns/README.md#getstatus) - Query per-profile action status within a campaign
- [`campaignsSync`](docs/sdks/campaigns/README.md#sync) - Mark actions as completed without performing them
- [`chatArchive`](docs/sdks/chat/README.md#archive) - Archive a conversation
- [`chatFindConversation`](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
- [`chatSearchConversations`](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
- [`chatUnreact`](docs/sdks/chat/README.md#unreact) - Remove emoji reaction from a message
- [`companyPagesGetAnalytics`](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics
- [`companyPagesGetPermissions`](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
- [`companyPagesGetPosts`](docs/sdks/companypages/README.md#getposts) - Get recent posts from a company page
- [`companyPagesList`](docs/sdks/companypages/README.md#list) - List company pages the user administers
- [`contactsUpsert`](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)
- [`linkedinActionsAcceptInvitation`](docs/sdks/linkedinactions1/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
- [`linkedInActionsCreateComment`](docs/sdks/linkedinactions2/README.md#createcomment) - Comment on a LinkedIn post
- [`linkedInActionsDeclineInvitation`](docs/sdks/linkedinactions2/README.md#declineinvitation) - Decline a connection invitation
- [`linkedinActionsEditComment`](docs/sdks/linkedinactions1/README.md#editcomment) - Edit a comment
- [`linkedinActionsEditPost`](docs/sdks/linkedinactions1/README.md#editpost) - Edit a post
- [`linkedinActionsFollowProfile`](docs/sdks/linkedinactions1/README.md#followprofile) - Follow a profile
- [`linkedInActionsLikeComment`](docs/sdks/linkedinactions2/README.md#likecomment) - Like a LinkedIn comment
- [`linkedinActionsLikePost`](docs/sdks/linkedinactions1/README.md#likepost) - Like a LinkedIn post
- [`linkedinActionsListInvitations`](docs/sdks/linkedinactions1/README.md#listinvitations) - List received LinkedIn connection invitations
- [`linkedInActionsPublishPost`](docs/sdks/linkedinactions2/README.md#publishpost) - Publish or schedule a LinkedIn post
- [`linkedinActionsReplyToComment`](docs/sdks/linkedinactions1/README.md#replytocomment) - Reply to a LinkedIn comment
- [`linkedinActionsRepostPost`](docs/sdks/linkedinactions1/README.md#repostpost) - Repost / share a post
- [`linkedInActionsSavePost`](docs/sdks/linkedinactions2/README.md#savepost) - Save a post
- [`linkedinActionsUnfollowCompany`](docs/sdks/linkedinactions1/README.md#unfollowcompany) - Unfollow a company
- [`linkedInActionsUnfollowProfile`](docs/sdks/linkedinactions2/README.md#unfollowprofile) - Unfollow a profile
- [`linkedinActionsUnlikeComment`](docs/sdks/linkedinactions1/README.md#unlikecomment) - Unlike a comment
- [`linkedinActionsUnlikePost`](docs/sdks/linkedinactions1/README.md#unlikepost) - Unlike a post
- [`linkedinActionsUnsavePost`](docs/sdks/linkedinactions1/README.md#unsavepost) - Unsave a post
- [`linkedinActionsWithdrawInvitation`](docs/sdks/linkedinactions1/README.md#withdrawinvitation) - Withdraw a sent connection invitation
- [`linkedinChatGetMessages`](docs/sdks/linkedinchat1/README.md#getmessages) - Read messages from a conversation
- [`linkedinChatGetUnreadCount`](docs/sdks/linkedinchat1/README.md#getunreadcount) - Get unread message count
- [`linkedinChatListArchived`](docs/sdks/linkedinchat1/README.md#listarchived) - List archived conversations
- [`linkedinChatListInboxConversations`](docs/sdks/linkedinchat1/README.md#listinboxconversations) - List LinkedIn inbox conversations
- [`linkedInChatListStarred`](docs/sdks/linkedinchat2/README.md#liststarred) - List starred conversations
- [`linkedinChatMarkAllRead`](docs/sdks/linkedinchat1/README.md#markallread) - Mark all conversations as read
- [`linkedInChatMarkSeen`](docs/sdks/linkedinchat2/README.md#markseen) - Mark a conversation as read
- [`linkedinChatReact`](docs/sdks/linkedinchat1/README.md#react) - React to a message with emoji
- [`linkedinChatSendTypingIndicator`](docs/sdks/linkedinchat1/README.md#sendtypingindicator) - Send typing indicator
- [`linkedInChatStar`](docs/sdks/linkedinchat2/README.md#star) - Star a conversation
- [`linkedInChatUnarchive`](docs/sdks/linkedinchat2/README.md#unarchive) - Unarchive a conversation
- [`linkedInChatUnstar`](docs/sdks/linkedinchat2/README.md#unstar) - Unstar a conversation
- [`linkedInScrapersCollectCommentReplies`](docs/sdks/linkedinscrapers2/README.md#collectcommentreplies) - Scrape replies to a LinkedIn comment
- [`linkedinScrapersCollectComments`](docs/sdks/linkedinscrapers1/README.md#collectcomments) - Scrape LinkedIn post comments
- [`linkedinScrapersCollectHashtagPosts`](docs/sdks/linkedinscrapers1/README.md#collecthashtagposts) - Collect posts from a hashtag
- [`linkedinScrapersCollectLikes`](docs/sdks/linkedinscrapers1/README.md#collectlikes) - Scrape LinkedIn post likes
- [`linkedInScrapersGetFeed`](docs/sdks/linkedinscrapers2/README.md#getfeed) - Get home feed
- [`linkedinScrapersListSavedPosts`](docs/sdks/linkedinscrapers1/README.md#listsavedposts) - List saved posts
- [`linkedinScrapersVisitCompany`](docs/sdks/linkedinscrapers1/README.md#visitcompany) - Visit LinkedIn company page and extract profile data
- [`linkedInSearchResolveParameters`](docs/sdks/linkedinsearch1/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)
- [`linkedInSearchSearch`](docs/sdks/linkedinsearch1/README.md#search) - Unified LinkedIn Search — posts, people, companies, jobs
- [`linkedinSearchSearchByUrl`](docs/sdks/linkedinsearch2/README.md#searchbyurl) - Search LinkedIn by URL
- [`linkedInSearchSearchCompanies`](docs/sdks/linkedinsearch1/README.md#searchcompanies) - Search LinkedIn Companies
- [`linkedinSearchSearchJobs`](docs/sdks/linkedinsearch2/README.md#searchjobs) - Search LinkedIn Jobs
- [`linkedinSearchSearchPeople`](docs/sdks/linkedinsearch2/README.md#searchpeople) - Search LinkedIn People
- [`linkedinSearchSearchPosts`](docs/sdks/linkedinsearch2/README.md#searchposts) - Search LinkedIn Posts
- [`profileGet`](docs/sdks/profile/README.md#get) - Get authenticated user's LinkedIn profile
- [`profileGetCredits`](docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance
- [`profileGetFollowerAnalytics`](docs/sdks/profile/README.md#getfolloweranalytics) - Get follower analytics
- [`profileGetFollowers`](docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
- [`profileGetLimits`](docs/sdks/profile/README.md#getlimits) - Get current LinkedIn rate limit status
- [`profileGetPostAnalytics`](docs/sdks/profile/README.md#getpostanalytics) - Get post analytics
- [`profileGetPosts`](docs/sdks/profile/README.md#getposts) - Get authenticated user's LinkedIn posts
- [`profileGetProfileViews`](docs/sdks/profile/README.md#getprofileviews) - Get profile views
- [`profileGetSearchAppearances`](docs/sdks/profile/README.md#getsearchappearances) - Get search appearances
- [`profileListAccounts`](docs/sdks/profile/README.md#listaccounts) - List all LinkedIn accounts for the authenticated user
- [`profileRefresh`](docs/sdks/profile/README.md#refresh) - Refresh authenticated user's LinkedIn profile
- [`profileUpdateAccount`](docs/sdks/profile/README.md#updateaccount) - Update a LinkedIn account (label, default)
- [`salesNavigatorSearchSearch`](docs/sdks/salesnavigatorsearch/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
- [`salesNavigatorSearchSearchCompanies`](docs/sdks/salesnavigatorsearch/README.md#searchcompanies) - Sales Navigator Company/Account Search
- [`salesNavSearchPeople`](docs/sdks/salesnav/README.md#searchpeople) - Sales Navigator People/Lead Search
- [`scrapersCollectPosts`](docs/sdks/scrapers/README.md#collectposts) - Scrape LinkedIn profile posts
- [`scrapersVisitProfile`](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
- ~~[`campaignsFilter`](docs/sdks/campaigns/README.md#filter)~~ - Check if campaign actions are completed :warning: **Deprecated**

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

[`BereachError`](./src/models/errors/bereach-error.ts) is the base class for all HTTP error responses. It has the following properties:

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
      if (error instanceof errors.CollectLinkedInLikesBadRequestError) {
        console.log(error.data$.success); // boolean
        console.log(error.data$.error); // operations.CollectLinkedInLikesBadRequestError
      }
    }
  }
}

run();

```

### Error Classes
**Primary error:**
* [`BereachError`](./src/models/errors/bereach-error.ts): The base class for HTTP error responses.

<details><summary>Less common errors (708)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/http-client-errors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/http-client-errors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/http-client-errors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/http-client-errors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/http-client-errors.ts): Unrecognised or unexpected error.


**Inherit from [`BereachError`](./src/models/errors/bereach-error.ts)**:
* [`CollectLinkedInLikesBadRequestError`](./src/models/errors/collect-linked-in-likes-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsBadRequestError`](./src/models/errors/collect-linked-in-comments-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyBadRequestError`](./src/models/errors/visit-linked-in-company-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsBadRequestError`](./src/models/errors/collect-saved-linked-in-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsBadRequestError`](./src/models/errors/collect-linked-in-hashtag-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesBadRequestError`](./src/models/errors/collect-linked-in-comment-replies-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedBadRequestError`](./src/models/errors/get-linked-in-feed-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsBadRequestError`](./src/models/errors/collect-linked-in-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileBadRequestError`](./src/models/errors/visit-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInBadRequestError`](./src/models/errors/search-linked-in-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesBadRequestError`](./src/models/errors/search-linked-in-companies-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersBadRequestError`](./src/models/errors/resolve-linked-in-search-parameters-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsBadRequestError`](./src/models/errors/search-linked-in-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleBadRequestError`](./src/models/errors/search-linked-in-people-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsBadRequestError`](./src/models/errors/search-linked-in-jobs-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlBadRequestError`](./src/models/errors/search-linked-in-by-url-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavBadRequestError`](./src/models/errors/search-sales-nav-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesBadRequestError`](./src/models/errors/search-sales-nav-companies-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleBadRequestError`](./src/models/errors/search-sales-nav-people-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileBadRequestError`](./src/models/errors/connect-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageBadRequestError`](./src/models/errors/send-linked-in-message-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsBadRequestError`](./src/models/errors/list-sent-linked-in-invitations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyBadRequestError`](./src/models/errors/follow-linked-in-company-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsBadRequestError`](./src/models/errors/list-linked-in-invitations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationBadRequestError`](./src/models/errors/accept-linked-in-invitation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentBadRequestError`](./src/models/errors/reply-to-linked-in-comment-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostBadRequestError`](./src/models/errors/like-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationBadRequestError`](./src/models/errors/withdraw-linked-in-invitation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileBadRequestError`](./src/models/errors/follow-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostBadRequestError`](./src/models/errors/edit-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentBadRequestError`](./src/models/errors/edit-linked-in-comment-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostBadRequestError`](./src/models/errors/repost-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostBadRequestError`](./src/models/errors/unlike-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentBadRequestError`](./src/models/errors/unlike-linked-in-comment-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostBadRequestError`](./src/models/errors/unsave-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyBadRequestError`](./src/models/errors/unfollow-linked-in-company-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentBadRequestError`](./src/models/errors/like-linked-in-comment-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostBadRequestError`](./src/models/errors/publish-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostBadRequestError`](./src/models/errors/comment-on-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationBadRequestError`](./src/models/errors/decline-linked-in-invitation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileBadRequestError`](./src/models/errors/unfollow-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostBadRequestError`](./src/models/errors/save-linked-in-post-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileBadRequestError`](./src/models/errors/get-my-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsBadRequestError`](./src/models/errors/list-linked-in-accounts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountBadRequestError`](./src/models/errors/update-linked-in-account-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileBadRequestError`](./src/models/errors/refresh-my-linked-in-profile-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsBadRequestError`](./src/models/errors/get-my-linked-in-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersBadRequestError`](./src/models/errors/get-my-linked-in-followers-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsBadRequestError`](./src/models/errors/get-my-limits-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsBadRequestError`](./src/models/errors/get-my-credits-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsBadRequestError`](./src/models/errors/get-linked-in-profile-views-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesBadRequestError`](./src/models/errors/get-linked-in-search-appearances-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsBadRequestError`](./src/models/errors/get-linked-in-post-analytics-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsBadRequestError`](./src/models/errors/get-linked-in-follower-analytics-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesBadRequestError`](./src/models/errors/list-linked-in-company-pages-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsBadRequestError`](./src/models/errors/get-company-page-posts-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsBadRequestError`](./src/models/errors/get-company-page-permissions-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsBadRequestError`](./src/models/errors/get-company-page-analytics-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsBadRequestError`](./src/models/errors/list-inbox-conversations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesBadRequestError`](./src/models/errors/get-conversation-messages-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadBadRequestError`](./src/models/errors/mark-all-conversations-read-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsBadRequestError`](./src/models/errors/list-archived-conversations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ReactToMessageBadRequestError`](./src/models/errors/react-to-message-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorBadRequestError`](./src/models/errors/send-typing-indicator-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountBadRequestError`](./src/models/errors/get-unread-count-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsBadRequestError`](./src/models/errors/search-linked-in-conversations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationBadRequestError`](./src/models/errors/find-linked-in-conversation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationBadRequestError`](./src/models/errors/archive-conversation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageBadRequestError`](./src/models/errors/unreact-to-message-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenBadRequestError`](./src/models/errors/mark-conversation-seen-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`StarConversationBadRequestError`](./src/models/errors/star-conversation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnstarConversationBadRequestError`](./src/models/errors/unstar-conversation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsBadRequestError`](./src/models/errors/list-starred-conversations-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationBadRequestError`](./src/models/errors/unarchive-conversation-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`FilterCampaignBadRequestError`](./src/models/errors/filter-campaign-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusBadRequestError`](./src/models/errors/get-campaign-status-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsBadRequestError`](./src/models/errors/sync-campaign-actions-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsBadRequestError`](./src/models/errors/get-campaign-stats-bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesUnauthorizedError`](./src/models/errors/collect-linked-in-likes-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsUnauthorizedError`](./src/models/errors/collect-linked-in-comments-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyUnauthorizedError`](./src/models/errors/visit-linked-in-company-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsUnauthorizedError`](./src/models/errors/collect-saved-linked-in-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsUnauthorizedError`](./src/models/errors/collect-linked-in-hashtag-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesUnauthorizedError`](./src/models/errors/collect-linked-in-comment-replies-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedUnauthorizedError`](./src/models/errors/get-linked-in-feed-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsUnauthorizedError`](./src/models/errors/collect-linked-in-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileUnauthorizedError`](./src/models/errors/visit-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInUnauthorizedError`](./src/models/errors/search-linked-in-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesUnauthorizedError`](./src/models/errors/search-linked-in-companies-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersUnauthorizedError`](./src/models/errors/resolve-linked-in-search-parameters-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsUnauthorizedError`](./src/models/errors/search-linked-in-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleUnauthorizedError`](./src/models/errors/search-linked-in-people-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsUnauthorizedError`](./src/models/errors/search-linked-in-jobs-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlUnauthorizedError`](./src/models/errors/search-linked-in-by-url-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavUnauthorizedError`](./src/models/errors/search-sales-nav-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesUnauthorizedError`](./src/models/errors/search-sales-nav-companies-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleUnauthorizedError`](./src/models/errors/search-sales-nav-people-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileUnauthorizedError`](./src/models/errors/connect-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageUnauthorizedError`](./src/models/errors/send-linked-in-message-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsUnauthorizedError`](./src/models/errors/list-sent-linked-in-invitations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyUnauthorizedError`](./src/models/errors/follow-linked-in-company-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsUnauthorizedError`](./src/models/errors/list-linked-in-invitations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationUnauthorizedError`](./src/models/errors/accept-linked-in-invitation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentUnauthorizedError`](./src/models/errors/reply-to-linked-in-comment-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostUnauthorizedError`](./src/models/errors/like-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationUnauthorizedError`](./src/models/errors/withdraw-linked-in-invitation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileUnauthorizedError`](./src/models/errors/follow-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostUnauthorizedError`](./src/models/errors/edit-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentUnauthorizedError`](./src/models/errors/edit-linked-in-comment-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostUnauthorizedError`](./src/models/errors/repost-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostUnauthorizedError`](./src/models/errors/unlike-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentUnauthorizedError`](./src/models/errors/unlike-linked-in-comment-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostUnauthorizedError`](./src/models/errors/unsave-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyUnauthorizedError`](./src/models/errors/unfollow-linked-in-company-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentUnauthorizedError`](./src/models/errors/like-linked-in-comment-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostUnauthorizedError`](./src/models/errors/publish-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostUnauthorizedError`](./src/models/errors/comment-on-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationUnauthorizedError`](./src/models/errors/decline-linked-in-invitation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileUnauthorizedError`](./src/models/errors/unfollow-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostUnauthorizedError`](./src/models/errors/save-linked-in-post-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileUnauthorizedError`](./src/models/errors/get-my-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsUnauthorizedError`](./src/models/errors/list-linked-in-accounts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountUnauthorizedError`](./src/models/errors/update-linked-in-account-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileUnauthorizedError`](./src/models/errors/refresh-my-linked-in-profile-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsUnauthorizedError`](./src/models/errors/get-my-linked-in-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersUnauthorizedError`](./src/models/errors/get-my-linked-in-followers-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsUnauthorizedError`](./src/models/errors/get-my-limits-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsUnauthorizedError`](./src/models/errors/get-my-credits-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsUnauthorizedError`](./src/models/errors/get-linked-in-profile-views-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesUnauthorizedError`](./src/models/errors/get-linked-in-search-appearances-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsUnauthorizedError`](./src/models/errors/get-linked-in-post-analytics-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsUnauthorizedError`](./src/models/errors/get-linked-in-follower-analytics-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesUnauthorizedError`](./src/models/errors/list-linked-in-company-pages-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsUnauthorizedError`](./src/models/errors/get-company-page-posts-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsUnauthorizedError`](./src/models/errors/get-company-page-permissions-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsUnauthorizedError`](./src/models/errors/get-company-page-analytics-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsUnauthorizedError`](./src/models/errors/list-inbox-conversations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesUnauthorizedError`](./src/models/errors/get-conversation-messages-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadUnauthorizedError`](./src/models/errors/mark-all-conversations-read-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsUnauthorizedError`](./src/models/errors/list-archived-conversations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ReactToMessageUnauthorizedError`](./src/models/errors/react-to-message-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorUnauthorizedError`](./src/models/errors/send-typing-indicator-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountUnauthorizedError`](./src/models/errors/get-unread-count-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsUnauthorizedError`](./src/models/errors/search-linked-in-conversations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationUnauthorizedError`](./src/models/errors/find-linked-in-conversation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationUnauthorizedError`](./src/models/errors/archive-conversation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageUnauthorizedError`](./src/models/errors/unreact-to-message-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenUnauthorizedError`](./src/models/errors/mark-conversation-seen-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`StarConversationUnauthorizedError`](./src/models/errors/star-conversation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnstarConversationUnauthorizedError`](./src/models/errors/unstar-conversation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsUnauthorizedError`](./src/models/errors/list-starred-conversations-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationUnauthorizedError`](./src/models/errors/unarchive-conversation-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`FilterCampaignUnauthorizedError`](./src/models/errors/filter-campaign-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusUnauthorizedError`](./src/models/errors/get-campaign-status-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsUnauthorizedError`](./src/models/errors/sync-campaign-actions-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsUnauthorizedError`](./src/models/errors/get-campaign-stats-unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesForbiddenError`](./src/models/errors/collect-linked-in-likes-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsForbiddenError`](./src/models/errors/collect-linked-in-comments-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyForbiddenError`](./src/models/errors/visit-linked-in-company-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsForbiddenError`](./src/models/errors/collect-saved-linked-in-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsForbiddenError`](./src/models/errors/collect-linked-in-hashtag-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesForbiddenError`](./src/models/errors/collect-linked-in-comment-replies-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedForbiddenError`](./src/models/errors/get-linked-in-feed-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsForbiddenError`](./src/models/errors/collect-linked-in-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileForbiddenError`](./src/models/errors/visit-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInForbiddenError`](./src/models/errors/search-linked-in-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesForbiddenError`](./src/models/errors/search-linked-in-companies-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersForbiddenError`](./src/models/errors/resolve-linked-in-search-parameters-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsForbiddenError`](./src/models/errors/search-linked-in-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleForbiddenError`](./src/models/errors/search-linked-in-people-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsForbiddenError`](./src/models/errors/search-linked-in-jobs-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlForbiddenError`](./src/models/errors/search-linked-in-by-url-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavForbiddenError`](./src/models/errors/search-sales-nav-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesForbiddenError`](./src/models/errors/search-sales-nav-companies-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleForbiddenError`](./src/models/errors/search-sales-nav-people-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileForbiddenError`](./src/models/errors/connect-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageForbiddenError`](./src/models/errors/send-linked-in-message-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsForbiddenError`](./src/models/errors/list-sent-linked-in-invitations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyForbiddenError`](./src/models/errors/follow-linked-in-company-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsForbiddenError`](./src/models/errors/list-linked-in-invitations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationForbiddenError`](./src/models/errors/accept-linked-in-invitation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentForbiddenError`](./src/models/errors/reply-to-linked-in-comment-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostForbiddenError`](./src/models/errors/like-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationForbiddenError`](./src/models/errors/withdraw-linked-in-invitation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileForbiddenError`](./src/models/errors/follow-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostForbiddenError`](./src/models/errors/edit-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentForbiddenError`](./src/models/errors/edit-linked-in-comment-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostForbiddenError`](./src/models/errors/repost-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostForbiddenError`](./src/models/errors/unlike-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentForbiddenError`](./src/models/errors/unlike-linked-in-comment-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostForbiddenError`](./src/models/errors/unsave-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyForbiddenError`](./src/models/errors/unfollow-linked-in-company-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentForbiddenError`](./src/models/errors/like-linked-in-comment-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostForbiddenError`](./src/models/errors/publish-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostForbiddenError`](./src/models/errors/comment-on-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationForbiddenError`](./src/models/errors/decline-linked-in-invitation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileForbiddenError`](./src/models/errors/unfollow-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostForbiddenError`](./src/models/errors/save-linked-in-post-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileForbiddenError`](./src/models/errors/get-my-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsForbiddenError`](./src/models/errors/list-linked-in-accounts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountForbiddenError`](./src/models/errors/update-linked-in-account-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileForbiddenError`](./src/models/errors/refresh-my-linked-in-profile-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsForbiddenError`](./src/models/errors/get-my-linked-in-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersForbiddenError`](./src/models/errors/get-my-linked-in-followers-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsForbiddenError`](./src/models/errors/get-my-limits-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsForbiddenError`](./src/models/errors/get-my-credits-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsForbiddenError`](./src/models/errors/get-linked-in-profile-views-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesForbiddenError`](./src/models/errors/get-linked-in-search-appearances-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsForbiddenError`](./src/models/errors/get-linked-in-post-analytics-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsForbiddenError`](./src/models/errors/get-linked-in-follower-analytics-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesForbiddenError`](./src/models/errors/list-linked-in-company-pages-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsForbiddenError`](./src/models/errors/get-company-page-posts-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsForbiddenError`](./src/models/errors/get-company-page-permissions-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsForbiddenError`](./src/models/errors/get-company-page-analytics-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsForbiddenError`](./src/models/errors/list-inbox-conversations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesForbiddenError`](./src/models/errors/get-conversation-messages-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadForbiddenError`](./src/models/errors/mark-all-conversations-read-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsForbiddenError`](./src/models/errors/list-archived-conversations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ReactToMessageForbiddenError`](./src/models/errors/react-to-message-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorForbiddenError`](./src/models/errors/send-typing-indicator-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountForbiddenError`](./src/models/errors/get-unread-count-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsForbiddenError`](./src/models/errors/search-linked-in-conversations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationForbiddenError`](./src/models/errors/find-linked-in-conversation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationForbiddenError`](./src/models/errors/archive-conversation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageForbiddenError`](./src/models/errors/unreact-to-message-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenForbiddenError`](./src/models/errors/mark-conversation-seen-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`StarConversationForbiddenError`](./src/models/errors/star-conversation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnstarConversationForbiddenError`](./src/models/errors/unstar-conversation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsForbiddenError`](./src/models/errors/list-starred-conversations-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationForbiddenError`](./src/models/errors/unarchive-conversation-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`FilterCampaignForbiddenError`](./src/models/errors/filter-campaign-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusForbiddenError`](./src/models/errors/get-campaign-status-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsForbiddenError`](./src/models/errors/sync-campaign-actions-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsForbiddenError`](./src/models/errors/get-campaign-stats-forbidden-error.ts): The client does not have access rights to the content. Status code `403`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesNotFoundError`](./src/models/errors/collect-linked-in-likes-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsNotFoundError`](./src/models/errors/collect-linked-in-comments-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyNotFoundError`](./src/models/errors/visit-linked-in-company-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsNotFoundError`](./src/models/errors/collect-saved-linked-in-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsNotFoundError`](./src/models/errors/collect-linked-in-hashtag-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesNotFoundError`](./src/models/errors/collect-linked-in-comment-replies-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedNotFoundError`](./src/models/errors/get-linked-in-feed-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsNotFoundError`](./src/models/errors/collect-linked-in-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileNotFoundError`](./src/models/errors/visit-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInNotFoundError`](./src/models/errors/search-linked-in-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesNotFoundError`](./src/models/errors/search-linked-in-companies-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersNotFoundError`](./src/models/errors/resolve-linked-in-search-parameters-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsNotFoundError`](./src/models/errors/search-linked-in-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleNotFoundError`](./src/models/errors/search-linked-in-people-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsNotFoundError`](./src/models/errors/search-linked-in-jobs-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlNotFoundError`](./src/models/errors/search-linked-in-by-url-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavNotFoundError`](./src/models/errors/search-sales-nav-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesNotFoundError`](./src/models/errors/search-sales-nav-companies-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleNotFoundError`](./src/models/errors/search-sales-nav-people-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileNotFoundError`](./src/models/errors/connect-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageNotFoundError`](./src/models/errors/send-linked-in-message-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsNotFoundError`](./src/models/errors/list-sent-linked-in-invitations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyNotFoundError`](./src/models/errors/follow-linked-in-company-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsNotFoundError`](./src/models/errors/list-linked-in-invitations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationNotFoundError`](./src/models/errors/accept-linked-in-invitation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentNotFoundError`](./src/models/errors/reply-to-linked-in-comment-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostNotFoundError`](./src/models/errors/like-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationNotFoundError`](./src/models/errors/withdraw-linked-in-invitation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileNotFoundError`](./src/models/errors/follow-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostNotFoundError`](./src/models/errors/edit-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentNotFoundError`](./src/models/errors/edit-linked-in-comment-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostNotFoundError`](./src/models/errors/repost-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostNotFoundError`](./src/models/errors/unlike-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentNotFoundError`](./src/models/errors/unlike-linked-in-comment-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostNotFoundError`](./src/models/errors/unsave-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyNotFoundError`](./src/models/errors/unfollow-linked-in-company-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentNotFoundError`](./src/models/errors/like-linked-in-comment-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostNotFoundError`](./src/models/errors/publish-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostNotFoundError`](./src/models/errors/comment-on-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationNotFoundError`](./src/models/errors/decline-linked-in-invitation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileNotFoundError`](./src/models/errors/unfollow-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostNotFoundError`](./src/models/errors/save-linked-in-post-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileNotFoundError`](./src/models/errors/get-my-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsNotFoundError`](./src/models/errors/list-linked-in-accounts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountNotFoundError`](./src/models/errors/update-linked-in-account-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileNotFoundError`](./src/models/errors/refresh-my-linked-in-profile-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsNotFoundError`](./src/models/errors/get-my-linked-in-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersNotFoundError`](./src/models/errors/get-my-linked-in-followers-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsNotFoundError`](./src/models/errors/get-my-limits-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsNotFoundError`](./src/models/errors/get-my-credits-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsNotFoundError`](./src/models/errors/get-linked-in-profile-views-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesNotFoundError`](./src/models/errors/get-linked-in-search-appearances-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsNotFoundError`](./src/models/errors/get-linked-in-post-analytics-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsNotFoundError`](./src/models/errors/get-linked-in-follower-analytics-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesNotFoundError`](./src/models/errors/list-linked-in-company-pages-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsNotFoundError`](./src/models/errors/get-company-page-posts-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsNotFoundError`](./src/models/errors/get-company-page-permissions-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsNotFoundError`](./src/models/errors/get-company-page-analytics-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsNotFoundError`](./src/models/errors/list-inbox-conversations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesNotFoundError`](./src/models/errors/get-conversation-messages-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadNotFoundError`](./src/models/errors/mark-all-conversations-read-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsNotFoundError`](./src/models/errors/list-archived-conversations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ReactToMessageNotFoundError`](./src/models/errors/react-to-message-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorNotFoundError`](./src/models/errors/send-typing-indicator-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountNotFoundError`](./src/models/errors/get-unread-count-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsNotFoundError`](./src/models/errors/search-linked-in-conversations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationNotFoundError`](./src/models/errors/find-linked-in-conversation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationNotFoundError`](./src/models/errors/archive-conversation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageNotFoundError`](./src/models/errors/unreact-to-message-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenNotFoundError`](./src/models/errors/mark-conversation-seen-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`StarConversationNotFoundError`](./src/models/errors/star-conversation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnstarConversationNotFoundError`](./src/models/errors/unstar-conversation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsNotFoundError`](./src/models/errors/list-starred-conversations-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationNotFoundError`](./src/models/errors/unarchive-conversation-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`FilterCampaignNotFoundError`](./src/models/errors/filter-campaign-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusNotFoundError`](./src/models/errors/get-campaign-status-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsNotFoundError`](./src/models/errors/sync-campaign-actions-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsNotFoundError`](./src/models/errors/get-campaign-stats-not-found-error.ts): The server cannot find the requested resource. Status code `404`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesConflictError`](./src/models/errors/collect-linked-in-likes-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsConflictError`](./src/models/errors/collect-linked-in-comments-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyConflictError`](./src/models/errors/visit-linked-in-company-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsConflictError`](./src/models/errors/collect-saved-linked-in-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsConflictError`](./src/models/errors/collect-linked-in-hashtag-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesConflictError`](./src/models/errors/collect-linked-in-comment-replies-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedConflictError`](./src/models/errors/get-linked-in-feed-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsConflictError`](./src/models/errors/collect-linked-in-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileConflictError`](./src/models/errors/visit-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConflictError`](./src/models/errors/search-linked-in-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesConflictError`](./src/models/errors/search-linked-in-companies-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersConflictError`](./src/models/errors/resolve-linked-in-search-parameters-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsConflictError`](./src/models/errors/search-linked-in-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleConflictError`](./src/models/errors/search-linked-in-people-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsConflictError`](./src/models/errors/search-linked-in-jobs-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlConflictError`](./src/models/errors/search-linked-in-by-url-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavConflictError`](./src/models/errors/search-sales-nav-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesConflictError`](./src/models/errors/search-sales-nav-companies-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleConflictError`](./src/models/errors/search-sales-nav-people-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileConflictError`](./src/models/errors/connect-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageConflictError`](./src/models/errors/send-linked-in-message-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsConflictError`](./src/models/errors/list-sent-linked-in-invitations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyConflictError`](./src/models/errors/follow-linked-in-company-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsConflictError`](./src/models/errors/list-linked-in-invitations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationConflictError`](./src/models/errors/accept-linked-in-invitation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentConflictError`](./src/models/errors/reply-to-linked-in-comment-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostConflictError`](./src/models/errors/like-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationConflictError`](./src/models/errors/withdraw-linked-in-invitation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileConflictError`](./src/models/errors/follow-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostConflictError`](./src/models/errors/edit-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentConflictError`](./src/models/errors/edit-linked-in-comment-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostConflictError`](./src/models/errors/repost-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostConflictError`](./src/models/errors/unlike-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentConflictError`](./src/models/errors/unlike-linked-in-comment-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostConflictError`](./src/models/errors/unsave-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyConflictError`](./src/models/errors/unfollow-linked-in-company-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentConflictError`](./src/models/errors/like-linked-in-comment-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostConflictError`](./src/models/errors/publish-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostConflictError`](./src/models/errors/comment-on-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationConflictError`](./src/models/errors/decline-linked-in-invitation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileConflictError`](./src/models/errors/unfollow-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostConflictError`](./src/models/errors/save-linked-in-post-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileConflictError`](./src/models/errors/get-my-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsConflictError`](./src/models/errors/list-linked-in-accounts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountConflictError`](./src/models/errors/update-linked-in-account-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileConflictError`](./src/models/errors/refresh-my-linked-in-profile-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsConflictError`](./src/models/errors/get-my-linked-in-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersConflictError`](./src/models/errors/get-my-linked-in-followers-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsConflictError`](./src/models/errors/get-my-limits-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsConflictError`](./src/models/errors/get-my-credits-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsConflictError`](./src/models/errors/get-linked-in-profile-views-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesConflictError`](./src/models/errors/get-linked-in-search-appearances-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsConflictError`](./src/models/errors/get-linked-in-post-analytics-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsConflictError`](./src/models/errors/get-linked-in-follower-analytics-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesConflictError`](./src/models/errors/list-linked-in-company-pages-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsConflictError`](./src/models/errors/get-company-page-posts-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsConflictError`](./src/models/errors/get-company-page-permissions-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsConflictError`](./src/models/errors/get-company-page-analytics-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsConflictError`](./src/models/errors/list-inbox-conversations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesConflictError`](./src/models/errors/get-conversation-messages-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadConflictError`](./src/models/errors/mark-all-conversations-read-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsConflictError`](./src/models/errors/list-archived-conversations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ReactToMessageConflictError`](./src/models/errors/react-to-message-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorConflictError`](./src/models/errors/send-typing-indicator-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountConflictError`](./src/models/errors/get-unread-count-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsConflictError`](./src/models/errors/search-linked-in-conversations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationConflictError`](./src/models/errors/find-linked-in-conversation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationConflictError`](./src/models/errors/archive-conversation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageConflictError`](./src/models/errors/unreact-to-message-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenConflictError`](./src/models/errors/mark-conversation-seen-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`StarConversationConflictError`](./src/models/errors/star-conversation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnstarConversationConflictError`](./src/models/errors/unstar-conversation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsConflictError`](./src/models/errors/list-starred-conversations-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationConflictError`](./src/models/errors/unarchive-conversation-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`FilterCampaignConflictError`](./src/models/errors/filter-campaign-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusConflictError`](./src/models/errors/get-campaign-status-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsConflictError`](./src/models/errors/sync-campaign-actions-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsConflictError`](./src/models/errors/get-campaign-stats-conflict-error.ts): The request conflicts with the current state of the server. Status code `409`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesGoneError`](./src/models/errors/collect-linked-in-likes-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsGoneError`](./src/models/errors/collect-linked-in-comments-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyGoneError`](./src/models/errors/visit-linked-in-company-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsGoneError`](./src/models/errors/collect-saved-linked-in-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsGoneError`](./src/models/errors/collect-linked-in-hashtag-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesGoneError`](./src/models/errors/collect-linked-in-comment-replies-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedGoneError`](./src/models/errors/get-linked-in-feed-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsGoneError`](./src/models/errors/collect-linked-in-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileGoneError`](./src/models/errors/visit-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInGoneError`](./src/models/errors/search-linked-in-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesGoneError`](./src/models/errors/search-linked-in-companies-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersGoneError`](./src/models/errors/resolve-linked-in-search-parameters-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsGoneError`](./src/models/errors/search-linked-in-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleGoneError`](./src/models/errors/search-linked-in-people-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsGoneError`](./src/models/errors/search-linked-in-jobs-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlGoneError`](./src/models/errors/search-linked-in-by-url-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavGoneError`](./src/models/errors/search-sales-nav-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesGoneError`](./src/models/errors/search-sales-nav-companies-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleGoneError`](./src/models/errors/search-sales-nav-people-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileGoneError`](./src/models/errors/connect-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageGoneError`](./src/models/errors/send-linked-in-message-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsGoneError`](./src/models/errors/list-sent-linked-in-invitations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyGoneError`](./src/models/errors/follow-linked-in-company-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsGoneError`](./src/models/errors/list-linked-in-invitations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationGoneError`](./src/models/errors/accept-linked-in-invitation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentGoneError`](./src/models/errors/reply-to-linked-in-comment-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostGoneError`](./src/models/errors/like-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationGoneError`](./src/models/errors/withdraw-linked-in-invitation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileGoneError`](./src/models/errors/follow-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostGoneError`](./src/models/errors/edit-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentGoneError`](./src/models/errors/edit-linked-in-comment-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostGoneError`](./src/models/errors/repost-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostGoneError`](./src/models/errors/unlike-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentGoneError`](./src/models/errors/unlike-linked-in-comment-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostGoneError`](./src/models/errors/unsave-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyGoneError`](./src/models/errors/unfollow-linked-in-company-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentGoneError`](./src/models/errors/like-linked-in-comment-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostGoneError`](./src/models/errors/publish-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostGoneError`](./src/models/errors/comment-on-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationGoneError`](./src/models/errors/decline-linked-in-invitation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileGoneError`](./src/models/errors/unfollow-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostGoneError`](./src/models/errors/save-linked-in-post-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileGoneError`](./src/models/errors/get-my-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsGoneError`](./src/models/errors/list-linked-in-accounts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountGoneError`](./src/models/errors/update-linked-in-account-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileGoneError`](./src/models/errors/refresh-my-linked-in-profile-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsGoneError`](./src/models/errors/get-my-linked-in-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersGoneError`](./src/models/errors/get-my-linked-in-followers-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsGoneError`](./src/models/errors/get-my-limits-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsGoneError`](./src/models/errors/get-my-credits-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsGoneError`](./src/models/errors/get-linked-in-profile-views-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesGoneError`](./src/models/errors/get-linked-in-search-appearances-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsGoneError`](./src/models/errors/get-linked-in-post-analytics-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsGoneError`](./src/models/errors/get-linked-in-follower-analytics-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesGoneError`](./src/models/errors/list-linked-in-company-pages-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsGoneError`](./src/models/errors/get-company-page-posts-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsGoneError`](./src/models/errors/get-company-page-permissions-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsGoneError`](./src/models/errors/get-company-page-analytics-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsGoneError`](./src/models/errors/list-inbox-conversations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesGoneError`](./src/models/errors/get-conversation-messages-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadGoneError`](./src/models/errors/mark-all-conversations-read-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsGoneError`](./src/models/errors/list-archived-conversations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ReactToMessageGoneError`](./src/models/errors/react-to-message-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorGoneError`](./src/models/errors/send-typing-indicator-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountGoneError`](./src/models/errors/get-unread-count-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsGoneError`](./src/models/errors/search-linked-in-conversations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationGoneError`](./src/models/errors/find-linked-in-conversation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationGoneError`](./src/models/errors/archive-conversation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageGoneError`](./src/models/errors/unreact-to-message-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenGoneError`](./src/models/errors/mark-conversation-seen-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`StarConversationGoneError`](./src/models/errors/star-conversation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnstarConversationGoneError`](./src/models/errors/unstar-conversation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsGoneError`](./src/models/errors/list-starred-conversations-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationGoneError`](./src/models/errors/unarchive-conversation-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`FilterCampaignGoneError`](./src/models/errors/filter-campaign-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusGoneError`](./src/models/errors/get-campaign-status-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsGoneError`](./src/models/errors/sync-campaign-actions-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsGoneError`](./src/models/errors/get-campaign-stats-gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesUnprocessableEntityError`](./src/models/errors/collect-linked-in-likes-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsUnprocessableEntityError`](./src/models/errors/collect-linked-in-comments-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyUnprocessableEntityError`](./src/models/errors/visit-linked-in-company-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsUnprocessableEntityError`](./src/models/errors/collect-saved-linked-in-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsUnprocessableEntityError`](./src/models/errors/collect-linked-in-hashtag-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesUnprocessableEntityError`](./src/models/errors/collect-linked-in-comment-replies-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedUnprocessableEntityError`](./src/models/errors/get-linked-in-feed-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsUnprocessableEntityError`](./src/models/errors/collect-linked-in-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileUnprocessableEntityError`](./src/models/errors/visit-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInUnprocessableEntityError`](./src/models/errors/search-linked-in-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesUnprocessableEntityError`](./src/models/errors/search-linked-in-companies-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersUnprocessableEntityError`](./src/models/errors/resolve-linked-in-search-parameters-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsUnprocessableEntityError`](./src/models/errors/search-linked-in-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleUnprocessableEntityError`](./src/models/errors/search-linked-in-people-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsUnprocessableEntityError`](./src/models/errors/search-linked-in-jobs-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlUnprocessableEntityError`](./src/models/errors/search-linked-in-by-url-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavUnprocessableEntityError`](./src/models/errors/search-sales-nav-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesUnprocessableEntityError`](./src/models/errors/search-sales-nav-companies-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleUnprocessableEntityError`](./src/models/errors/search-sales-nav-people-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileUnprocessableEntityError`](./src/models/errors/connect-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageUnprocessableEntityError`](./src/models/errors/send-linked-in-message-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsUnprocessableEntityError`](./src/models/errors/list-sent-linked-in-invitations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyUnprocessableEntityError`](./src/models/errors/follow-linked-in-company-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsUnprocessableEntityError`](./src/models/errors/list-linked-in-invitations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationUnprocessableEntityError`](./src/models/errors/accept-linked-in-invitation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentUnprocessableEntityError`](./src/models/errors/reply-to-linked-in-comment-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostUnprocessableEntityError`](./src/models/errors/like-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationUnprocessableEntityError`](./src/models/errors/withdraw-linked-in-invitation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileUnprocessableEntityError`](./src/models/errors/follow-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostUnprocessableEntityError`](./src/models/errors/edit-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentUnprocessableEntityError`](./src/models/errors/edit-linked-in-comment-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostUnprocessableEntityError`](./src/models/errors/repost-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostUnprocessableEntityError`](./src/models/errors/unlike-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentUnprocessableEntityError`](./src/models/errors/unlike-linked-in-comment-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostUnprocessableEntityError`](./src/models/errors/unsave-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyUnprocessableEntityError`](./src/models/errors/unfollow-linked-in-company-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentUnprocessableEntityError`](./src/models/errors/like-linked-in-comment-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostUnprocessableEntityError`](./src/models/errors/publish-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostUnprocessableEntityError`](./src/models/errors/comment-on-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationUnprocessableEntityError`](./src/models/errors/decline-linked-in-invitation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileUnprocessableEntityError`](./src/models/errors/unfollow-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostUnprocessableEntityError`](./src/models/errors/save-linked-in-post-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileUnprocessableEntityError`](./src/models/errors/get-my-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsUnprocessableEntityError`](./src/models/errors/list-linked-in-accounts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountUnprocessableEntityError`](./src/models/errors/update-linked-in-account-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileUnprocessableEntityError`](./src/models/errors/refresh-my-linked-in-profile-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsUnprocessableEntityError`](./src/models/errors/get-my-linked-in-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersUnprocessableEntityError`](./src/models/errors/get-my-linked-in-followers-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsUnprocessableEntityError`](./src/models/errors/get-my-limits-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsUnprocessableEntityError`](./src/models/errors/get-my-credits-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsUnprocessableEntityError`](./src/models/errors/get-linked-in-profile-views-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesUnprocessableEntityError`](./src/models/errors/get-linked-in-search-appearances-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsUnprocessableEntityError`](./src/models/errors/get-linked-in-post-analytics-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsUnprocessableEntityError`](./src/models/errors/get-linked-in-follower-analytics-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesUnprocessableEntityError`](./src/models/errors/list-linked-in-company-pages-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsUnprocessableEntityError`](./src/models/errors/get-company-page-posts-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsUnprocessableEntityError`](./src/models/errors/get-company-page-permissions-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsUnprocessableEntityError`](./src/models/errors/get-company-page-analytics-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsUnprocessableEntityError`](./src/models/errors/list-inbox-conversations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesUnprocessableEntityError`](./src/models/errors/get-conversation-messages-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadUnprocessableEntityError`](./src/models/errors/mark-all-conversations-read-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsUnprocessableEntityError`](./src/models/errors/list-archived-conversations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ReactToMessageUnprocessableEntityError`](./src/models/errors/react-to-message-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorUnprocessableEntityError`](./src/models/errors/send-typing-indicator-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountUnprocessableEntityError`](./src/models/errors/get-unread-count-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsUnprocessableEntityError`](./src/models/errors/search-linked-in-conversations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationUnprocessableEntityError`](./src/models/errors/find-linked-in-conversation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationUnprocessableEntityError`](./src/models/errors/archive-conversation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageUnprocessableEntityError`](./src/models/errors/unreact-to-message-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenUnprocessableEntityError`](./src/models/errors/mark-conversation-seen-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`StarConversationUnprocessableEntityError`](./src/models/errors/star-conversation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnstarConversationUnprocessableEntityError`](./src/models/errors/unstar-conversation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsUnprocessableEntityError`](./src/models/errors/list-starred-conversations-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationUnprocessableEntityError`](./src/models/errors/unarchive-conversation-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`FilterCampaignUnprocessableEntityError`](./src/models/errors/filter-campaign-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusUnprocessableEntityError`](./src/models/errors/get-campaign-status-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsUnprocessableEntityError`](./src/models/errors/sync-campaign-actions-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsUnprocessableEntityError`](./src/models/errors/get-campaign-stats-unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesTooManyRequestsError`](./src/models/errors/collect-linked-in-likes-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsTooManyRequestsError`](./src/models/errors/collect-linked-in-comments-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyTooManyRequestsError`](./src/models/errors/visit-linked-in-company-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsTooManyRequestsError`](./src/models/errors/collect-saved-linked-in-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsTooManyRequestsError`](./src/models/errors/collect-linked-in-hashtag-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesTooManyRequestsError`](./src/models/errors/collect-linked-in-comment-replies-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedTooManyRequestsError`](./src/models/errors/get-linked-in-feed-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsTooManyRequestsError`](./src/models/errors/collect-linked-in-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileTooManyRequestsError`](./src/models/errors/visit-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInTooManyRequestsError`](./src/models/errors/search-linked-in-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesTooManyRequestsError`](./src/models/errors/search-linked-in-companies-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersTooManyRequestsError`](./src/models/errors/resolve-linked-in-search-parameters-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsTooManyRequestsError`](./src/models/errors/search-linked-in-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleTooManyRequestsError`](./src/models/errors/search-linked-in-people-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsTooManyRequestsError`](./src/models/errors/search-linked-in-jobs-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlTooManyRequestsError`](./src/models/errors/search-linked-in-by-url-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavTooManyRequestsError`](./src/models/errors/search-sales-nav-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesTooManyRequestsError`](./src/models/errors/search-sales-nav-companies-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleTooManyRequestsError`](./src/models/errors/search-sales-nav-people-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileTooManyRequestsError`](./src/models/errors/connect-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageTooManyRequestsError`](./src/models/errors/send-linked-in-message-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsTooManyRequestsError`](./src/models/errors/list-sent-linked-in-invitations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyTooManyRequestsError`](./src/models/errors/follow-linked-in-company-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsTooManyRequestsError`](./src/models/errors/list-linked-in-invitations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationTooManyRequestsError`](./src/models/errors/accept-linked-in-invitation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentTooManyRequestsError`](./src/models/errors/reply-to-linked-in-comment-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostTooManyRequestsError`](./src/models/errors/like-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationTooManyRequestsError`](./src/models/errors/withdraw-linked-in-invitation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileTooManyRequestsError`](./src/models/errors/follow-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostTooManyRequestsError`](./src/models/errors/edit-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentTooManyRequestsError`](./src/models/errors/edit-linked-in-comment-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostTooManyRequestsError`](./src/models/errors/repost-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostTooManyRequestsError`](./src/models/errors/unlike-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentTooManyRequestsError`](./src/models/errors/unlike-linked-in-comment-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostTooManyRequestsError`](./src/models/errors/unsave-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyTooManyRequestsError`](./src/models/errors/unfollow-linked-in-company-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentTooManyRequestsError`](./src/models/errors/like-linked-in-comment-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostTooManyRequestsError`](./src/models/errors/publish-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostTooManyRequestsError`](./src/models/errors/comment-on-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationTooManyRequestsError`](./src/models/errors/decline-linked-in-invitation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileTooManyRequestsError`](./src/models/errors/unfollow-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostTooManyRequestsError`](./src/models/errors/save-linked-in-post-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileTooManyRequestsError`](./src/models/errors/get-my-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsTooManyRequestsError`](./src/models/errors/list-linked-in-accounts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountTooManyRequestsError`](./src/models/errors/update-linked-in-account-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileTooManyRequestsError`](./src/models/errors/refresh-my-linked-in-profile-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsTooManyRequestsError`](./src/models/errors/get-my-linked-in-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersTooManyRequestsError`](./src/models/errors/get-my-linked-in-followers-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsTooManyRequestsError`](./src/models/errors/get-my-limits-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsTooManyRequestsError`](./src/models/errors/get-my-credits-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsTooManyRequestsError`](./src/models/errors/get-linked-in-profile-views-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesTooManyRequestsError`](./src/models/errors/get-linked-in-search-appearances-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsTooManyRequestsError`](./src/models/errors/get-linked-in-post-analytics-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsTooManyRequestsError`](./src/models/errors/get-linked-in-follower-analytics-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesTooManyRequestsError`](./src/models/errors/list-linked-in-company-pages-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsTooManyRequestsError`](./src/models/errors/get-company-page-posts-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsTooManyRequestsError`](./src/models/errors/get-company-page-permissions-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsTooManyRequestsError`](./src/models/errors/get-company-page-analytics-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsTooManyRequestsError`](./src/models/errors/list-inbox-conversations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesTooManyRequestsError`](./src/models/errors/get-conversation-messages-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadTooManyRequestsError`](./src/models/errors/mark-all-conversations-read-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsTooManyRequestsError`](./src/models/errors/list-archived-conversations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ReactToMessageTooManyRequestsError`](./src/models/errors/react-to-message-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorTooManyRequestsError`](./src/models/errors/send-typing-indicator-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountTooManyRequestsError`](./src/models/errors/get-unread-count-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsTooManyRequestsError`](./src/models/errors/search-linked-in-conversations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationTooManyRequestsError`](./src/models/errors/find-linked-in-conversation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationTooManyRequestsError`](./src/models/errors/archive-conversation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageTooManyRequestsError`](./src/models/errors/unreact-to-message-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenTooManyRequestsError`](./src/models/errors/mark-conversation-seen-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`StarConversationTooManyRequestsError`](./src/models/errors/star-conversation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnstarConversationTooManyRequestsError`](./src/models/errors/unstar-conversation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsTooManyRequestsError`](./src/models/errors/list-starred-conversations-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationTooManyRequestsError`](./src/models/errors/unarchive-conversation-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`FilterCampaignTooManyRequestsError`](./src/models/errors/filter-campaign-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusTooManyRequestsError`](./src/models/errors/get-campaign-status-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsTooManyRequestsError`](./src/models/errors/sync-campaign-actions-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsTooManyRequestsError`](./src/models/errors/get-campaign-stats-too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInLikesInternalServerError`](./src/models/errors/collect-linked-in-likes-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentsInternalServerError`](./src/models/errors/collect-linked-in-comments-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInCompanyInternalServerError`](./src/models/errors/visit-linked-in-company-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CollectSavedLinkedInPostsInternalServerError`](./src/models/errors/collect-saved-linked-in-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInHashtagPostsInternalServerError`](./src/models/errors/collect-linked-in-hashtag-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInCommentRepliesInternalServerError`](./src/models/errors/collect-linked-in-comment-replies-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFeedInternalServerError`](./src/models/errors/get-linked-in-feed-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CollectLinkedInPostsInternalServerError`](./src/models/errors/collect-linked-in-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`VisitLinkedInProfileInternalServerError`](./src/models/errors/visit-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInInternalServerError`](./src/models/errors/search-linked-in-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInCompaniesInternalServerError`](./src/models/errors/search-linked-in-companies-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ResolveLinkedInSearchParametersInternalServerError`](./src/models/errors/resolve-linked-in-search-parameters-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPostsInternalServerError`](./src/models/errors/search-linked-in-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInPeopleInternalServerError`](./src/models/errors/search-linked-in-people-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInJobsInternalServerError`](./src/models/errors/search-linked-in-jobs-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInByUrlInternalServerError`](./src/models/errors/search-linked-in-by-url-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavInternalServerError`](./src/models/errors/search-sales-nav-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavCompaniesInternalServerError`](./src/models/errors/search-sales-nav-companies-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchSalesNavPeopleInternalServerError`](./src/models/errors/search-sales-nav-people-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ConnectLinkedInProfileInternalServerError`](./src/models/errors/connect-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SendLinkedInMessageInternalServerError`](./src/models/errors/send-linked-in-message-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListSentLinkedInInvitationsInternalServerError`](./src/models/errors/list-sent-linked-in-invitations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInCompanyInternalServerError`](./src/models/errors/follow-linked-in-company-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListLinkedInInvitationsInternalServerError`](./src/models/errors/list-linked-in-invitations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`AcceptLinkedInInvitationInternalServerError`](./src/models/errors/accept-linked-in-invitation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ReplyToLinkedInCommentInternalServerError`](./src/models/errors/reply-to-linked-in-comment-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInPostInternalServerError`](./src/models/errors/like-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`WithdrawLinkedInInvitationInternalServerError`](./src/models/errors/withdraw-linked-in-invitation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`FollowLinkedInProfileInternalServerError`](./src/models/errors/follow-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`EditLinkedInPostInternalServerError`](./src/models/errors/edit-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`EditLinkedInCommentInternalServerError`](./src/models/errors/edit-linked-in-comment-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`RepostLinkedInPostInternalServerError`](./src/models/errors/repost-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInPostInternalServerError`](./src/models/errors/unlike-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnlikeLinkedInCommentInternalServerError`](./src/models/errors/unlike-linked-in-comment-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnsaveLinkedInPostInternalServerError`](./src/models/errors/unsave-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInCompanyInternalServerError`](./src/models/errors/unfollow-linked-in-company-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`LikeLinkedInCommentInternalServerError`](./src/models/errors/like-linked-in-comment-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`PublishLinkedInPostInternalServerError`](./src/models/errors/publish-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`CommentOnLinkedInPostInternalServerError`](./src/models/errors/comment-on-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`DeclineLinkedInInvitationInternalServerError`](./src/models/errors/decline-linked-in-invitation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnfollowLinkedInProfileInternalServerError`](./src/models/errors/unfollow-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SaveLinkedInPostInternalServerError`](./src/models/errors/save-linked-in-post-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInProfileInternalServerError`](./src/models/errors/get-my-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListLinkedInAccountsInternalServerError`](./src/models/errors/list-linked-in-accounts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UpdateLinkedInAccountInternalServerError`](./src/models/errors/update-linked-in-account-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`RefreshMyLinkedInProfileInternalServerError`](./src/models/errors/refresh-my-linked-in-profile-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInPostsInternalServerError`](./src/models/errors/get-my-linked-in-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetMyLinkedInFollowersInternalServerError`](./src/models/errors/get-my-linked-in-followers-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetMyLimitsInternalServerError`](./src/models/errors/get-my-limits-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetMyCreditsInternalServerError`](./src/models/errors/get-my-credits-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetLinkedInProfileViewsInternalServerError`](./src/models/errors/get-linked-in-profile-views-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetLinkedInSearchAppearancesInternalServerError`](./src/models/errors/get-linked-in-search-appearances-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetLinkedInPostAnalyticsInternalServerError`](./src/models/errors/get-linked-in-post-analytics-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetLinkedInFollowerAnalyticsInternalServerError`](./src/models/errors/get-linked-in-follower-analytics-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListLinkedInCompanyPagesInternalServerError`](./src/models/errors/list-linked-in-company-pages-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePostsInternalServerError`](./src/models/errors/get-company-page-posts-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetCompanyPagePermissionsInternalServerError`](./src/models/errors/get-company-page-permissions-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetCompanyPageAnalyticsInternalServerError`](./src/models/errors/get-company-page-analytics-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListInboxConversationsInternalServerError`](./src/models/errors/list-inbox-conversations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetConversationMessagesInternalServerError`](./src/models/errors/get-conversation-messages-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`MarkAllConversationsReadInternalServerError`](./src/models/errors/mark-all-conversations-read-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListArchivedConversationsInternalServerError`](./src/models/errors/list-archived-conversations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ReactToMessageInternalServerError`](./src/models/errors/react-to-message-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SendTypingIndicatorInternalServerError`](./src/models/errors/send-typing-indicator-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetUnreadCountInternalServerError`](./src/models/errors/get-unread-count-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SearchLinkedInConversationsInternalServerError`](./src/models/errors/search-linked-in-conversations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`FindLinkedInConversationInternalServerError`](./src/models/errors/find-linked-in-conversation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ArchiveConversationInternalServerError`](./src/models/errors/archive-conversation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnreactToMessageInternalServerError`](./src/models/errors/unreact-to-message-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`MarkConversationSeenInternalServerError`](./src/models/errors/mark-conversation-seen-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`StarConversationInternalServerError`](./src/models/errors/star-conversation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnstarConversationInternalServerError`](./src/models/errors/unstar-conversation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ListStarredConversationsInternalServerError`](./src/models/errors/list-starred-conversations-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`UnarchiveConversationInternalServerError`](./src/models/errors/unarchive-conversation-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`FilterCampaignInternalServerError`](./src/models/errors/filter-campaign-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatusInternalServerError`](./src/models/errors/get-campaign-status-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`SyncCampaignActionsInternalServerError`](./src/models/errors/sync-campaign-actions-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`GetCampaignStatsInternalServerError`](./src/models/errors/get-campaign-stats-internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`. Applicable to 1 of 79 methods.*
* [`ResponseValidationError`](./src/models/errors/response-validation-error.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
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

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
* [stats](docs/sdks/campaigns/README.md#stats) - Get aggregate campaign statistics

### [Chat](docs/sdks/chat/README.md)

* [searchConversations](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
* [findConversation](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
* [getMessages](docs/sdks/chat/README.md#getmessages) - Read messages from a conversation
* [listStarred](docs/sdks/chat/README.md#liststarred) - List starred conversations
* [archive](docs/sdks/chat/README.md#archive) - Archive a conversation
* [listArchived](docs/sdks/chat/README.md#listarchived) - List archived conversations
* [unreact](docs/sdks/chat/README.md#unreact) - Remove emoji reaction from a message
* [getUnreadCount](docs/sdks/chat/README.md#getunreadcount) - Get unread message count

### [CompanyPages](docs/sdks/companypages/README.md)

* [list](docs/sdks/companypages/README.md#list) - List company pages the user administers
* [getPosts](docs/sdks/companypages/README.md#getposts) - Get recent posts from a company page
* [getPermissions](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
* [getAnalytics](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics

### [Contacts](docs/sdks/contacts/README.md)

* [upsert](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)
* [search](docs/sdks/contacts/README.md#search) - Search and filter contacts
* [get](docs/sdks/contacts/README.md#get) - Get a single contact with activities and campaigns
* [update](docs/sdks/contacts/README.md#update) - Update a contact
* [listActivities](docs/sdks/contacts/README.md#listactivities) - List activities for a contact
* [addActivities](docs/sdks/contacts/README.md#addactivities) - Log activities for a contact
* [bulkUpdate](docs/sdks/contacts/README.md#bulkupdate) - Bulk update contacts
* [stats](docs/sdks/contacts/README.md#stats) - Get contact funnel statistics
* [listAgentStates](docs/sdks/contacts/README.md#listagentstates) - List all agent state entries
* [getAgentState](docs/sdks/contacts/README.md#getagentstate) - Get agent state by key
* [setAgentState](docs/sdks/contacts/README.md#setagentstate) - Set agent state by key
* [patchAgentState](docs/sdks/contacts/README.md#patchagentstate) - Merge-update agent state by key
* [deleteAgentState](docs/sdks/contacts/README.md#deleteagentstate) - Delete agent state by key
* [listCampaigns](docs/sdks/contacts/README.md#listcampaigns) - List campaigns
* [createCampaign](docs/sdks/contacts/README.md#createcampaign) - Create a lead-gen campaign
* [getCampaign](docs/sdks/contacts/README.md#getcampaign) - Get a single campaign
* [updateCampaign](docs/sdks/contacts/README.md#updatecampaign) - Update campaign settings
* [deleteCampaign](docs/sdks/contacts/README.md#deletecampaign) - Delete a campaign
* [campaignStatusTransition](docs/sdks/contacts/README.md#campaignstatustransition) - Campaign state transition
* [listByCampaign](docs/sdks/contacts/README.md#listbycampaign) - List contacts in a campaign
* [addToCampaign](docs/sdks/contacts/README.md#addtocampaign) - Add contacts to a campaign
* [getByUrl](docs/sdks/contacts/README.md#getbyurl) - Look up contact by LinkedIn URL

### [Context](docs/sdks/context/README.md)

* [listEntries](docs/sdks/context/README.md#listentries) - List context entries
* [set](docs/sdks/context/README.md#set) - Create or update a context entry
* [delete](docs/sdks/context/README.md#delete) - Delete a context entry

### [Cron](docs/sdks/cron/README.md)

* [listSchedules](docs/sdks/cron/README.md#listschedules) - List active cron schedules
* [updateSchedule](docs/sdks/cron/README.md#updateschedule) - Pause, resume, or delete a cron schedule

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

* [listInbox](docs/sdks/linkedinchat1/README.md#listinbox) - List LinkedIn inbox conversations
* [markAllRead](docs/sdks/linkedinchat1/README.md#markallread) - Mark all conversations as read
* [react](docs/sdks/linkedinchat1/README.md#react) - React to a message with emoji
* [sendTypingIndicator](docs/sdks/linkedinchat1/README.md#sendtypingindicator) - Send typing indicator

### [LinkedInChat](docs/sdks/linkedinchat2/README.md)

* [markSeen](docs/sdks/linkedinchat2/README.md#markseen) - Mark a conversation as read
* [star](docs/sdks/linkedinchat2/README.md#star) - Star a conversation
* [unstar](docs/sdks/linkedinchat2/README.md#unstar) - Unstar a conversation
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
* [switchAccount](docs/sdks/profile/README.md#switchaccount) - Switch active LinkedIn account
* [listConnections](docs/sdks/profile/README.md#listconnections) - List LinkedIn connections

### [SalesNav](docs/sdks/salesnav/README.md)

* [searchPeople](docs/sdks/salesnav/README.md#searchpeople) - Sales Navigator People/Lead Search

### [SalesNavigatorSearch](docs/sdks/salesnavigatorsearch/README.md)

* [search](docs/sdks/salesnavigatorsearch/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
* [searchCompanies](docs/sdks/salesnavigatorsearch/README.md#searchcompanies) - Sales Navigator Company/Account Search

### [ScheduledMessages](docs/sdks/scheduledmessages/README.md)

* [list](docs/sdks/scheduledmessages/README.md#list) - List scheduled messages
* [create](docs/sdks/scheduledmessages/README.md#create) - Create a draft DM
* [batchSchedule](docs/sdks/scheduledmessages/README.md#batchschedule) - Batch-schedule drafts for auto-send
* [cancel](docs/sdks/scheduledmessages/README.md#cancel) - Cancel scheduled or draft messages

### [Scrapers](docs/sdks/scrapers/README.md)

* [collectPosts](docs/sdks/scrapers/README.md#collectposts) - Scrape LinkedIn profile posts
* [visitProfile](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
* [bulkVisitProfile](docs/sdks/scrapers/README.md#bulkvisitprofile) - Queue bulk LinkedIn profile visits (fire-and-forget)
* [bulkVisitBatchStatus](docs/sdks/scrapers/README.md#bulkvisitbatchstatus) - Get bulk visit batch status

### [Search](docs/sdks/search/README.md)

* [resolveParameters](docs/sdks/search/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)

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
- [`campaignsGetStatus`](docs/sdks/campaigns/README.md#getstatus) - Query per-profile action status within a campaign
- [`campaignsStats`](docs/sdks/campaigns/README.md#stats) - Get aggregate campaign statistics
- [`campaignsSync`](docs/sdks/campaigns/README.md#sync) - Mark actions as completed without performing them
- [`chatArchive`](docs/sdks/chat/README.md#archive) - Archive a conversation
- [`chatFindConversation`](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
- [`chatGetMessages`](docs/sdks/chat/README.md#getmessages) - Read messages from a conversation
- [`chatGetUnreadCount`](docs/sdks/chat/README.md#getunreadcount) - Get unread message count
- [`chatListArchived`](docs/sdks/chat/README.md#listarchived) - List archived conversations
- [`chatListStarred`](docs/sdks/chat/README.md#liststarred) - List starred conversations
- [`chatSearchConversations`](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
- [`chatUnreact`](docs/sdks/chat/README.md#unreact) - Remove emoji reaction from a message
- [`companyPagesGetAnalytics`](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics
- [`companyPagesGetPermissions`](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
- [`companyPagesGetPosts`](docs/sdks/companypages/README.md#getposts) - Get recent posts from a company page
- [`companyPagesList`](docs/sdks/companypages/README.md#list) - List company pages the user administers
- [`contactsAddActivities`](docs/sdks/contacts/README.md#addactivities) - Log activities for a contact
- [`contactsAddToCampaign`](docs/sdks/contacts/README.md#addtocampaign) - Add contacts to a campaign
- [`contactsBulkUpdate`](docs/sdks/contacts/README.md#bulkupdate) - Bulk update contacts
- [`contactsCampaignStatusTransition`](docs/sdks/contacts/README.md#campaignstatustransition) - Campaign state transition
- [`contactsCreateCampaign`](docs/sdks/contacts/README.md#createcampaign) - Create a lead-gen campaign
- [`contactsDeleteAgentState`](docs/sdks/contacts/README.md#deleteagentstate) - Delete agent state by key
- [`contactsDeleteCampaign`](docs/sdks/contacts/README.md#deletecampaign) - Delete a campaign
- [`contactsGet`](docs/sdks/contacts/README.md#get) - Get a single contact with activities and campaigns
- [`contactsGetAgentState`](docs/sdks/contacts/README.md#getagentstate) - Get agent state by key
- [`contactsGetByUrl`](docs/sdks/contacts/README.md#getbyurl) - Look up contact by LinkedIn URL
- [`contactsGetCampaign`](docs/sdks/contacts/README.md#getcampaign) - Get a single campaign
- [`contactsListActivities`](docs/sdks/contacts/README.md#listactivities) - List activities for a contact
- [`contactsListAgentStates`](docs/sdks/contacts/README.md#listagentstates) - List all agent state entries
- [`contactsListByCampaign`](docs/sdks/contacts/README.md#listbycampaign) - List contacts in a campaign
- [`contactsListCampaigns`](docs/sdks/contacts/README.md#listcampaigns) - List campaigns
- [`contactsPatchAgentState`](docs/sdks/contacts/README.md#patchagentstate) - Merge-update agent state by key
- [`contactsSearch`](docs/sdks/contacts/README.md#search) - Search and filter contacts
- [`contactsSetAgentState`](docs/sdks/contacts/README.md#setagentstate) - Set agent state by key
- [`contactsStats`](docs/sdks/contacts/README.md#stats) - Get contact funnel statistics
- [`contactsUpdate`](docs/sdks/contacts/README.md#update) - Update a contact
- [`contactsUpdateCampaign`](docs/sdks/contacts/README.md#updatecampaign) - Update campaign settings
- [`contactsUpsert`](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)
- [`contextDelete`](docs/sdks/context/README.md#delete) - Delete a context entry
- [`contextListEntries`](docs/sdks/context/README.md#listentries) - List context entries
- [`contextSet`](docs/sdks/context/README.md#set) - Create or update a context entry
- [`cronListSchedules`](docs/sdks/cron/README.md#listschedules) - List active cron schedules
- [`cronUpdateSchedule`](docs/sdks/cron/README.md#updateschedule) - Pause, resume, or delete a cron schedule
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
- [`linkedinChatListInbox`](docs/sdks/linkedinchat1/README.md#listinbox) - List LinkedIn inbox conversations
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
- [`profileListConnections`](docs/sdks/profile/README.md#listconnections) - List LinkedIn connections
- [`profileRefresh`](docs/sdks/profile/README.md#refresh) - Refresh authenticated user's LinkedIn profile
- [`profileSwitchAccount`](docs/sdks/profile/README.md#switchaccount) - Switch active LinkedIn account
- [`profileUpdateAccount`](docs/sdks/profile/README.md#updateaccount) - Update a LinkedIn account (label, default)
- [`salesNavigatorSearchSearch`](docs/sdks/salesnavigatorsearch/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
- [`salesNavigatorSearchSearchCompanies`](docs/sdks/salesnavigatorsearch/README.md#searchcompanies) - Sales Navigator Company/Account Search
- [`salesNavSearchPeople`](docs/sdks/salesnav/README.md#searchpeople) - Sales Navigator People/Lead Search
- [`scheduledMessagesBatchSchedule`](docs/sdks/scheduledmessages/README.md#batchschedule) - Batch-schedule drafts for auto-send
- [`scheduledMessagesCancel`](docs/sdks/scheduledmessages/README.md#cancel) - Cancel scheduled or draft messages
- [`scheduledMessagesCreate`](docs/sdks/scheduledmessages/README.md#create) - Create a draft DM
- [`scheduledMessagesList`](docs/sdks/scheduledmessages/README.md#list) - List scheduled messages
- [`scrapersBulkVisitBatchStatus`](docs/sdks/scrapers/README.md#bulkvisitbatchstatus) - Get bulk visit batch status
- [`scrapersBulkVisitProfile`](docs/sdks/scrapers/README.md#bulkvisitprofile) - Queue bulk LinkedIn profile visits (fire-and-forget)
- [`scrapersCollectPosts`](docs/sdks/scrapers/README.md#collectposts) - Scrape LinkedIn profile posts
- [`scrapersVisitProfile`](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
- [`searchResolveParameters`](docs/sdks/search/README.md#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)
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
      if (error instanceof errors.BadRequestError) {
        console.log(error.data$.success); // boolean
        console.log(error.data$.error); // operations.CollectLikesBadRequestError
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`BereachError`](./src/models/errors/bereach-error.ts): The base class for HTTP error responses.
  * [`BadRequestError`](./src/models/errors/bad-request-error.ts): The server cannot or will not process the request due to something that is perceived to be a client error. Status code `400`.
  * [`UnauthorizedError`](./src/models/errors/unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. Status code `401`.
  * [`ForbiddenError`](./src/models/errors/forbidden-error.ts): The client does not have access rights to the content. Status code `403`.
  * [`NotFoundError`](./src/models/errors/not-found-error.ts): The server cannot find the requested resource. Status code `404`.
  * [`ConflictError`](./src/models/errors/conflict-error.ts): The request conflicts with the current state of the server. Status code `409`.
  * [`GoneError`](./src/models/errors/gone-error.ts): The requested content has been permanently deleted from the server. Status code `410`.
  * [`UnprocessableEntityError`](./src/models/errors/unprocessable-entity-error.ts): The request was well-formed but was unable to be followed due to semantic errors. Status code `422`.
  * [`TooManyRequestsError`](./src/models/errors/too-many-requests-error.ts): Rate limit exceeded. Read error.retryAfter for the wait time in seconds. Status code `429`.
  * [`InternalServerError`](./src/models/errors/internal-server-error.ts): The server encountered a situation it does not know how to handle. Status code `500`.
  * [`BadGatewayError`](./src/models/errors/bad-gateway-error.ts): LinkedIn returned a server error or the proxy connection failed. Retry after a few seconds. Status code `502`.
  * [`ServiceUnavailableError`](./src/models/errors/service-unavailable-error.ts): Proxy capacity temporarily exceeded. Retry after a few seconds. Status code `503`.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/http-client-errors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/http-client-errors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/http-client-errors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/http-client-errors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/http-client-errors.ts): Unrecognised or unexpected error.


**Inherit from [`BereachError`](./src/models/errors/bereach-error.ts)**:
* [`ResponseValidationError`](./src/models/errors/response-validation-error.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Select Server by Index

You can override the default server globally by passing a server index to the `serverIdx: number` optional parameter when initializing the SDK client instance. The selected server will then be used as the default on the operations that use it. This table lists the indexes associated with the available servers:

| #   | Server                         | Description    |
| --- | ------------------------------ | -------------- |
| 0   | `https://api.berea.ch`         | Production API |
| 1   | `https://api-staging.berea.ch` | Staging API    |

#### Example

```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  serverIdx: 0,
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

### Override Server URL Per-Client

The default server can also be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  serverURL: "https://api-staging.berea.ch",
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

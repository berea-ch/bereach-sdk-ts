# bereach

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *bereach* API.

[![Built by Speakeasy](https://img.shields.io/badge/Built_by-SPEAKEASY-374151?style=for-the-badge&labelColor=f3f4f6)](https://www.speakeasy.com/?utm_source=bereach&utm_campaign=typescript)
[![License: MIT](https://img.shields.io/badge/LICENSE_//_MIT-3b5bdb?style=for-the-badge&labelColor=eff6ff)](https://opensource.org/licenses/MIT)


<br /><br />
> [!IMPORTANT]
> This SDK is not yet ready for production use. To complete setup please follow the steps outlined in your [workspace](https://app.speakeasy.com/org/bereach-h29/bereach). Delete this section before > publishing to a package manager.

<!-- Start Summary [summary] -->
## Summary

BeReach API: BeReach | Agentic lead generation and outreach API
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
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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

* [connectProfile](docs/sdks/actions/README.md#connectprofile) - Send LinkedIn connection requests
* [listInvitations](docs/sdks/actions/README.md#listinvitations) - List received LinkedIn connection invitations
* [acceptInvitation](docs/sdks/actions/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
* [sendMessage](docs/sdks/actions/README.md#sendmessage) - Send LinkedIn message
* [replyToComment](docs/sdks/actions/README.md#replytocomment) - Reply to a LinkedIn comment
* [likeComment](docs/sdks/actions/README.md#likecomment) - Like a LinkedIn comment
* [createComment](docs/sdks/actions/README.md#createcomment) - Comment on a LinkedIn post
* [likePost](docs/sdks/actions/README.md#likepost) - Like a LinkedIn post
* [listSentInvitations](docs/sdks/actions/README.md#listsentinvitations) - List sent connection invitations
* [followProfile](docs/sdks/actions/README.md#followprofile) - Follow a profile
* [unfollowProfile](docs/sdks/actions/README.md#unfollowprofile) - Unfollow a profile
* [editPost](docs/sdks/actions/README.md#editpost) - Edit a post
* [editComment](docs/sdks/actions/README.md#editcomment) - Edit a comment
* [editProfile](docs/sdks/actions/README.md#editprofile) - Edit LinkedIn profile headline/summary
* [unlikePost](docs/sdks/actions/README.md#unlikepost) - Unlike a post
* [unlikeComment](docs/sdks/actions/README.md#unlikecomment) - Unlike a comment
* [deleteComment](docs/sdks/actions/README.md#deletecomment) - Delete one of your LinkedIn comments
* [followCompany](docs/sdks/actions/README.md#followcompany) - Follow a company
* [unfollowCompany](docs/sdks/actions/README.md#unfollowcompany) - Unfollow a company

### [Chat](docs/sdks/chat/README.md)

* [listInbox](docs/sdks/chat/README.md#listinbox) - List LinkedIn inbox conversations
* [searchConversations](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
* [findConversation](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
* [getMessages](docs/sdks/chat/README.md#getmessages) - Read messages from a conversation
* [markSeen](docs/sdks/chat/README.md#markseen) - Mark a conversation as read
* [markAllRead](docs/sdks/chat/README.md#markallread) - Mark all conversations as read
* [getUnreadCount](docs/sdks/chat/README.md#getunreadcount) - Get unread message count
* [getConversationSummary](docs/sdks/chat/README.md#getconversationsummary) - Get conversation summary for a contact
* [saveConversationSummary](docs/sdks/chat/README.md#saveconversationsummary) - Save conversation summary for a contact

### [CompanyPages](docs/sdks/companypages/README.md)

* [list](docs/sdks/companypages/README.md#list) - List company pages the user administers
* [posts](docs/sdks/companypages/README.md#posts) - Get recent posts from a company page
* [getPermissions](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
* [getAnalytics](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics

### [Contacts](docs/sdks/contacts/README.md)

* [upsert](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)
* [search](docs/sdks/contacts/README.md#search) - Search and filter contacts
* [get](docs/sdks/contacts/README.md#get) - Get a single contact with activities and campaigns
* [update](docs/sdks/contacts/README.md#update) - Update a contact
* [listActivities](docs/sdks/contacts/README.md#listactivities) - List activities for a contact
* [addActivities](docs/sdks/contacts/README.md#addactivities) - Log activities for a contact
* [discard](docs/sdks/contacts/README.md#discard) - Discard or restore people, in bulk
* [stats](docs/sdks/contacts/README.md#stats) - Get contact funnel statistics
* [listCampaigns](docs/sdks/contacts/README.md#listcampaigns) - List campaigns
* [createCampaign](docs/sdks/contacts/README.md#createcampaign) - Create a lead-gen campaign
* [listByCampaign](docs/sdks/contacts/README.md#listbycampaign) - List contacts in a campaign
* [addToCampaign](docs/sdks/contacts/README.md#addtocampaign) - Add contacts to a campaign
* [getByUrl](docs/sdks/contacts/README.md#getbyurl) - Look up contact by LinkedIn URL

### [Context](docs/sdks/context/README.md)

* [listEntries](docs/sdks/context/README.md#listentries) - List context entries
* [set](docs/sdks/context/README.md#set) - Create or update a context entry
* [delete](docs/sdks/context/README.md#delete) - Delete a context entry

### [Profile](docs/sdks/profile/README.md)

* [get](docs/sdks/profile/README.md#get) - Get authenticated user's LinkedIn profile
* [listAccounts](docs/sdks/profile/README.md#listaccounts) - List all LinkedIn accounts for the authenticated user
* [updateAccount](docs/sdks/profile/README.md#updateaccount) - Update a LinkedIn account (label, default)
* [getFollowers](docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
* [getLimits](docs/sdks/profile/README.md#getlimits) - Get current LinkedIn quota status
* [getConnectionStatus](docs/sdks/profile/README.md#getconnectionstatus) - Get the state of outgoing connection requests
* [getCredits](docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance
* [switchAccount](docs/sdks/profile/README.md#switchaccount) - Switch active LinkedIn account
* [listConnections](docs/sdks/profile/README.md#listconnections) - List LinkedIn connections
* [getMyActivity](docs/sdks/profile/README.md#getmyactivity) - Get recent activity (comments or reactions)
* [getMyPosts](docs/sdks/profile/README.md#getmyposts) - Get the authenticated user's own posts
* [getSettings](docs/sdks/profile/README.md#getsettings) - Get account settings
* [patchSettings](docs/sdks/profile/README.md#patchsettings) - Update account settings
* [getApiToken](docs/sdks/profile/README.md#getapitoken) - Get API token
* [createApiToken](docs/sdks/profile/README.md#createapitoken) - Create API token
* [deleteApiToken](docs/sdks/profile/README.md#deleteapitoken) - Delete API token

### [Public](docs/sdks/public/README.md)

* [publicProfile](docs/sdks/public/README.md#publicprofile) - Read a public profile
* [publicFindPeople](docs/sdks/public/README.md#publicfindpeople) - Find people from public data
* [publicFindCompanies](docs/sdks/public/README.md#publicfindcompanies) - Find companies from public data
* [publicCompany](docs/sdks/public/README.md#publiccompany) - Read a public company page
* [publicPostEngagers](docs/sdks/public/README.md#publicpostengagers) - Read a public post and its commenters
* [publicFindPosts](docs/sdks/public/README.md#publicfindposts) - Find public posts by topic
* [publicFindJobs](docs/sdks/public/README.md#publicfindjobs) - Find public job postings
* [publicEnrich](docs/sdks/public/README.md#publicenrich) - Publicly re-fetch a list of contacts

### [SalesNav](docs/sdks/salesnav/README.md)

* [search](docs/sdks/salesnav/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
* [people](docs/sdks/salesnav/README.md#people) - Sales Navigator People/Lead Search
* [companies](docs/sdks/salesnav/README.md#companies) - Sales Navigator Company/Account Search

### [ScheduledMessages](docs/sdks/scheduledmessages/README.md)

* [list](docs/sdks/scheduledmessages/README.md#list) - List scheduled messages
* [create](docs/sdks/scheduledmessages/README.md#create) - Create a draft DM
* [batchSchedule](docs/sdks/scheduledmessages/README.md#batchschedule) - Batch-schedule drafts for auto-send
* [update](docs/sdks/scheduledmessages/README.md#update) - Edit a draft DM
* [cancel](docs/sdks/scheduledmessages/README.md#cancel) - Cancel scheduled or draft messages
* [reviewDrafts](docs/sdks/scheduledmessages/README.md#reviewdrafts) - Batch approve/reject draft DMs

### [Scrapers](docs/sdks/scrapers/README.md)

* [collectEngagers](docs/sdks/scrapers/README.md#collectengagers) - Collect people on a post
* [collectPosts](docs/sdks/scrapers/README.md#collectposts) - Collect posts of a profile
* [visitProfile](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
* [getFeed](docs/sdks/scrapers/README.md#getfeed) - Get home feed

### [Search](docs/sdks/search/README.md)

* [employees](docs/sdks/search/README.md#employees) - Search people at a company
* [posts](docs/sdks/search/README.md#posts) - Search LinkedIn Posts
* [people](docs/sdks/search/README.md#people) - Search LinkedIn People
* [companies](docs/sdks/search/README.md#companies) - Search LinkedIn Companies
* [jobs](docs/sdks/search/README.md#jobs) - Search LinkedIn Jobs
* [byUrl](docs/sdks/search/README.md#byurl) - Search LinkedIn by URL
* [listSalesNavFilters](docs/sdks/search/README.md#listsalesnavfilters) - List the Sales Navigator filters available for this seat
* [listSalesNavPersonas](docs/sdks/search/README.md#listsalesnavpersonas) - List the user's saved Sales Navigator personas
* [listSalesNavSavedSearches](docs/sdks/search/README.md#listsalesnavsavedsearches) - List the user's saved Sales Navigator searches
* [searchParameters](docs/sdks/search/README.md#searchparameters) - Turn text into the ids LinkedIn filters take
* [resolveProfiles](docs/sdks/search/README.md#resolveprofiles) - Upgrade encrypted or Sales Navigator profile links to canonical ones

### [Settings](docs/sdks/settings/README.md)

* [getDmPollingSettings](docs/sdks/settings/README.md#getdmpollingsettings) - Get DM polling settings
* [patchDmPollingSettings](docs/sdks/settings/README.md#patchdmpollingsettings) - Update DM polling settings

### [Tasks](docs/sdks/tasks/README.md)

* [eventsFeed](docs/sdks/tasks/README.md#eventsfeed) - Poll for events
* [agentSnapshot](docs/sdks/tasks/README.md#agentsnapshot) - Agent session snapshot

### [Workspace](docs/sdks/workspace/README.md)

* [deleteWorkspaceAccount](docs/sdks/workspace/README.md#deleteworkspaceaccount) - Remove a LinkedIn account
* [upgradeWorkspaceAccount](docs/sdks/workspace/README.md#upgradeworkspaceaccount) - Upgrade or downgrade account plan
* [createWorkspaceInvite](docs/sdks/workspace/README.md#createworkspaceinvite) - Create or list workspace invites
* [deleteWorkspaceInvite](docs/sdks/workspace/README.md#deleteworkspaceinvite) - Delete a workspace invite

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

- [`actionsAcceptInvitation`](docs/sdks/actions/README.md#acceptinvitation) - Accept a LinkedIn connection invitation
- [`actionsConnectProfile`](docs/sdks/actions/README.md#connectprofile) - Send LinkedIn connection requests
- [`actionsCreateComment`](docs/sdks/actions/README.md#createcomment) - Comment on a LinkedIn post
- [`actionsDeleteComment`](docs/sdks/actions/README.md#deletecomment) - Delete one of your LinkedIn comments
- [`actionsEditComment`](docs/sdks/actions/README.md#editcomment) - Edit a comment
- [`actionsEditPost`](docs/sdks/actions/README.md#editpost) - Edit a post
- [`actionsEditProfile`](docs/sdks/actions/README.md#editprofile) - Edit LinkedIn profile headline/summary
- [`actionsFollowCompany`](docs/sdks/actions/README.md#followcompany) - Follow a company
- [`actionsFollowProfile`](docs/sdks/actions/README.md#followprofile) - Follow a profile
- [`actionsLikeComment`](docs/sdks/actions/README.md#likecomment) - Like a LinkedIn comment
- [`actionsLikePost`](docs/sdks/actions/README.md#likepost) - Like a LinkedIn post
- [`actionsListInvitations`](docs/sdks/actions/README.md#listinvitations) - List received LinkedIn connection invitations
- [`actionsListSentInvitations`](docs/sdks/actions/README.md#listsentinvitations) - List sent connection invitations
- [`actionsReplyToComment`](docs/sdks/actions/README.md#replytocomment) - Reply to a LinkedIn comment
- [`actionsSendMessage`](docs/sdks/actions/README.md#sendmessage) - Send LinkedIn message
- [`actionsUnfollowCompany`](docs/sdks/actions/README.md#unfollowcompany) - Unfollow a company
- [`actionsUnfollowProfile`](docs/sdks/actions/README.md#unfollowprofile) - Unfollow a profile
- [`actionsUnlikeComment`](docs/sdks/actions/README.md#unlikecomment) - Unlike a comment
- [`actionsUnlikePost`](docs/sdks/actions/README.md#unlikepost) - Unlike a post
- [`chatFindConversation`](docs/sdks/chat/README.md#findconversation) - Find a conversation with a specific person
- [`chatGetConversationSummary`](docs/sdks/chat/README.md#getconversationsummary) - Get conversation summary for a contact
- [`chatGetMessages`](docs/sdks/chat/README.md#getmessages) - Read messages from a conversation
- [`chatGetUnreadCount`](docs/sdks/chat/README.md#getunreadcount) - Get unread message count
- [`chatListInbox`](docs/sdks/chat/README.md#listinbox) - List LinkedIn inbox conversations
- [`chatMarkAllRead`](docs/sdks/chat/README.md#markallread) - Mark all conversations as read
- [`chatMarkSeen`](docs/sdks/chat/README.md#markseen) - Mark a conversation as read
- [`chatSaveConversationSummary`](docs/sdks/chat/README.md#saveconversationsummary) - Save conversation summary for a contact
- [`chatSearchConversations`](docs/sdks/chat/README.md#searchconversations) - Search LinkedIn conversations
- [`companyPagesGetAnalytics`](docs/sdks/companypages/README.md#getanalytics) - Get company page overview analytics
- [`companyPagesGetPermissions`](docs/sdks/companypages/README.md#getpermissions) - Get admin permissions for a company page
- [`companyPagesList`](docs/sdks/companypages/README.md#list) - List company pages the user administers
- [`companyPagesPosts`](docs/sdks/companypages/README.md#posts) - Get recent posts from a company page
- [`contactsAddActivities`](docs/sdks/contacts/README.md#addactivities) - Log activities for a contact
- [`contactsAddToCampaign`](docs/sdks/contacts/README.md#addtocampaign) - Add contacts to a campaign
- [`contactsCreateCampaign`](docs/sdks/contacts/README.md#createcampaign) - Create a lead-gen campaign
- [`contactsDiscard`](docs/sdks/contacts/README.md#discard) - Discard or restore people, in bulk
- [`contactsGet`](docs/sdks/contacts/README.md#get) - Get a single contact with activities and campaigns
- [`contactsGetByUrl`](docs/sdks/contacts/README.md#getbyurl) - Look up contact by LinkedIn URL
- [`contactsListActivities`](docs/sdks/contacts/README.md#listactivities) - List activities for a contact
- [`contactsListByCampaign`](docs/sdks/contacts/README.md#listbycampaign) - List contacts in a campaign
- [`contactsListCampaigns`](docs/sdks/contacts/README.md#listcampaigns) - List campaigns
- [`contactsSearch`](docs/sdks/contacts/README.md#search) - Search and filter contacts
- [`contactsStats`](docs/sdks/contacts/README.md#stats) - Get contact funnel statistics
- [`contactsUpdate`](docs/sdks/contacts/README.md#update) - Update a contact
- [`contactsUpsert`](docs/sdks/contacts/README.md#upsert) - Create or upsert contacts (no campaign required)
- [`contextDelete`](docs/sdks/context/README.md#delete) - Delete a context entry
- [`contextListEntries`](docs/sdks/context/README.md#listentries) - List context entries
- [`contextSet`](docs/sdks/context/README.md#set) - Create or update a context entry
- [`profileCreateApiToken`](docs/sdks/profile/README.md#createapitoken) - Create API token
- [`profileDeleteApiToken`](docs/sdks/profile/README.md#deleteapitoken) - Delete API token
- [`profileGet`](docs/sdks/profile/README.md#get) - Get authenticated user's LinkedIn profile
- [`profileGetApiToken`](docs/sdks/profile/README.md#getapitoken) - Get API token
- [`profileGetConnectionStatus`](docs/sdks/profile/README.md#getconnectionstatus) - Get the state of outgoing connection requests
- [`profileGetCredits`](docs/sdks/profile/README.md#getcredits) - Get current BeReach credit balance
- [`profileGetFollowers`](docs/sdks/profile/README.md#getfollowers) - Get authenticated user's LinkedIn followers
- [`profileGetLimits`](docs/sdks/profile/README.md#getlimits) - Get current LinkedIn quota status
- [`profileGetMyActivity`](docs/sdks/profile/README.md#getmyactivity) - Get recent activity (comments or reactions)
- [`profileGetMyPosts`](docs/sdks/profile/README.md#getmyposts) - Get the authenticated user's own posts
- [`profileGetSettings`](docs/sdks/profile/README.md#getsettings) - Get account settings
- [`profileListAccounts`](docs/sdks/profile/README.md#listaccounts) - List all LinkedIn accounts for the authenticated user
- [`profileListConnections`](docs/sdks/profile/README.md#listconnections) - List LinkedIn connections
- [`profilePatchSettings`](docs/sdks/profile/README.md#patchsettings) - Update account settings
- [`profileSwitchAccount`](docs/sdks/profile/README.md#switchaccount) - Switch active LinkedIn account
- [`profileUpdateAccount`](docs/sdks/profile/README.md#updateaccount) - Update a LinkedIn account (label, default)
- [`publicPublicCompany`](docs/sdks/public/README.md#publiccompany) - Read a public company page
- [`publicPublicEnrich`](docs/sdks/public/README.md#publicenrich) - Publicly re-fetch a list of contacts
- [`publicPublicFindCompanies`](docs/sdks/public/README.md#publicfindcompanies) - Find companies from public data
- [`publicPublicFindJobs`](docs/sdks/public/README.md#publicfindjobs) - Find public job postings
- [`publicPublicFindPeople`](docs/sdks/public/README.md#publicfindpeople) - Find people from public data
- [`publicPublicFindPosts`](docs/sdks/public/README.md#publicfindposts) - Find public posts by topic
- [`publicPublicPostEngagers`](docs/sdks/public/README.md#publicpostengagers) - Read a public post and its commenters
- [`publicPublicProfile`](docs/sdks/public/README.md#publicprofile) - Read a public profile
- [`salesNavCompanies`](docs/sdks/salesnav/README.md#companies) - Sales Navigator Company/Account Search
- [`salesNavPeople`](docs/sdks/salesnav/README.md#people) - Sales Navigator People/Lead Search
- [`salesNavSearch`](docs/sdks/salesnav/README.md#search) - Sales Navigator Search — leads (people) & accounts (companies)
- [`scheduledMessagesBatchSchedule`](docs/sdks/scheduledmessages/README.md#batchschedule) - Batch-schedule drafts for auto-send
- [`scheduledMessagesCancel`](docs/sdks/scheduledmessages/README.md#cancel) - Cancel scheduled or draft messages
- [`scheduledMessagesCreate`](docs/sdks/scheduledmessages/README.md#create) - Create a draft DM
- [`scheduledMessagesList`](docs/sdks/scheduledmessages/README.md#list) - List scheduled messages
- [`scheduledMessagesReviewDrafts`](docs/sdks/scheduledmessages/README.md#reviewdrafts) - Batch approve/reject draft DMs
- [`scheduledMessagesUpdate`](docs/sdks/scheduledmessages/README.md#update) - Edit a draft DM
- [`scrapersCollectEngagers`](docs/sdks/scrapers/README.md#collectengagers) - Collect people on a post
- [`scrapersCollectPosts`](docs/sdks/scrapers/README.md#collectposts) - Collect posts of a profile
- [`scrapersGetFeed`](docs/sdks/scrapers/README.md#getfeed) - Get home feed
- [`scrapersVisitProfile`](docs/sdks/scrapers/README.md#visitprofile) - Visit LinkedIn profile and extract contact data
- [`searchByUrl`](docs/sdks/search/README.md#byurl) - Search LinkedIn by URL
- [`searchCompanies`](docs/sdks/search/README.md#companies) - Search LinkedIn Companies
- [`searchEmployees`](docs/sdks/search/README.md#employees) - Search people at a company
- [`searchJobs`](docs/sdks/search/README.md#jobs) - Search LinkedIn Jobs
- [`searchListSalesNavFilters`](docs/sdks/search/README.md#listsalesnavfilters) - List the Sales Navigator filters available for this seat
- [`searchListSalesNavPersonas`](docs/sdks/search/README.md#listsalesnavpersonas) - List the user's saved Sales Navigator personas
- [`searchListSalesNavSavedSearches`](docs/sdks/search/README.md#listsalesnavsavedsearches) - List the user's saved Sales Navigator searches
- [`searchPeople`](docs/sdks/search/README.md#people) - Search LinkedIn People
- [`searchPosts`](docs/sdks/search/README.md#posts) - Search LinkedIn Posts
- [`searchResolveProfiles`](docs/sdks/search/README.md#resolveprofiles) - Upgrade encrypted or Sales Navigator profile links to canonical ones
- [`searchSearchParameters`](docs/sdks/search/README.md#searchparameters) - Turn text into the ids LinkedIn filters take
- [`settingsGetDmPollingSettings`](docs/sdks/settings/README.md#getdmpollingsettings) - Get DM polling settings
- [`settingsPatchDmPollingSettings`](docs/sdks/settings/README.md#patchdmpollingsettings) - Update DM polling settings
- [`tasksAgentSnapshot`](docs/sdks/tasks/README.md#agentsnapshot) - Agent session snapshot
- [`tasksEventsFeed`](docs/sdks/tasks/README.md#eventsfeed) - Poll for events
- [`workspaceCreateWorkspaceInvite`](docs/sdks/workspace/README.md#createworkspaceinvite) - Create or list workspace invites
- [`workspaceDeleteWorkspaceAccount`](docs/sdks/workspace/README.md#deleteworkspaceaccount) - Remove a LinkedIn account
- [`workspaceDeleteWorkspaceInvite`](docs/sdks/workspace/README.md#deleteworkspaceinvite) - Delete a workspace invite
- [`workspaceUpgradeWorkspaceAccount`](docs/sdks/workspace/README.md#upgradeworkspaceaccount) - Upgrade or downgrade account plan

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
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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
    const result = await bereach.scrapers.collectEngagers({
      postUrls: [
        "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
      ],
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
        console.log(error.data$.error); // operations.CollectEngagersBadRequestError
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
  * [`UnauthorizedError`](./src/models/errors/unauthorized-error.ts): Although HTTP specifies "unauthorized", this response means "unauthenticated". Authenticate to continue. NOTE: 401 is also returned with code "linkedin_not_connected" when the caller IS authenticated but has no connected LinkedIn account — connect LinkedIn (not re-authenticate) to continue. Status code `401`.
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

| #   | Server                           | Description    |
| --- | -------------------------------- | -------------- |
| 0   | `https://api.bereach.ai`         | Production API |
| 1   | `https://api-staging.bereach.ai` | Staging API    |

#### Example

```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  serverIdx: 0,
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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
  serverURL: "https://api-staging.bereach.ai",
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.scrapers.collectEngagers({
    postUrls: [
      "https://www.linkedin.com/feed/update/urn:li:activity:1234567890123456789/",
    ],
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

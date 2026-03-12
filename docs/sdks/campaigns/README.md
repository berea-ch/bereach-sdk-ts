# Campaigns

## Overview

Endpoints for managing campaigns and workflow filtering

### Available Operations

* [~~filter~~](#filter) - Check if campaign actions are completed :warning: **Deprecated**
* [getStatus](#getstatus) - Query per-profile action status within a campaign
* [sync](#sync) - Mark actions as completed without performing them
* [getStats](#getstats) - Get aggregate campaign statistics

## ~~filter~~

Check if all provided actionSlugs are completed for a given campaignSlug. Used by n8n workflows to determine if a flow should be skipped.

> :warning: **DEPRECATED**: This will be removed in a future release, please migrate away from it as soon as possible.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="filterCampaign" method="get" path="/campaigns/{campaignSlug}/filter" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.campaigns.filter({
    campaignSlug: "<value>",
    actionSlugs: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { campaignsFilter } from "bereach/funcs/campaigns-filter.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await campaignsFilter(bereach, {
    campaignSlug: "<value>",
    actionSlugs: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("campaignsFilter failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.FilterCampaignRequest](../../models/operations/filter-campaign-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.FilterCampaignResponse](../../models/operations/filter-campaign-response.md)\>**

### Errors

| Error Type                                    | Status Code                                   | Content Type                                  |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| errors.FilterCampaignBadRequestError          | 400                                           | application/json                              |
| errors.FilterCampaignUnauthorizedError        | 401                                           | application/json                              |
| errors.FilterCampaignForbiddenError           | 403                                           | application/json                              |
| errors.FilterCampaignNotFoundError            | 404                                           | application/json                              |
| errors.FilterCampaignConflictError            | 409                                           | application/json                              |
| errors.FilterCampaignGoneError                | 410                                           | application/json                              |
| errors.FilterCampaignUnprocessableEntityError | 422                                           | application/json                              |
| errors.FilterCampaignTooManyRequestsError     | 429                                           | application/json                              |
| errors.FilterCampaignInternalServerError      | 500                                           | application/json                              |
| errors.BereachDefaultError                    | 4XX, 5XX                                      | \*/\*                                         |

## getStatus

Returns which actions (message, reply, like, visit, connect) have been completed for each profile within a campaign. Replaces the slug-based filter endpoint — query by profile URLs instead of building slug lists. 0 credits, no rate limit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getCampaignStatus" method="post" path="/campaigns/{campaignSlug}/status" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.campaigns.getStatus({
    campaignSlug: "<value>",
    body: {
      profiles: [
        "https://www.linkedin.com/in/john-doe",
        "https://www.linkedin.com/in/jane-smith",
      ],
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { campaignsGetStatus } from "bereach/funcs/campaigns-get-status.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await campaignsGetStatus(bereach, {
    campaignSlug: "<value>",
    body: {
      profiles: [
        "https://www.linkedin.com/in/john-doe",
        "https://www.linkedin.com/in/jane-smith",
      ],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("campaignsGetStatus failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetCampaignStatusRequest](../../models/operations/get-campaign-status-request.md)                                                                                  | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetCampaignStatusResponse](../../models/operations/get-campaign-status-response.md)\>**

### Errors

| Error Type                                       | Status Code                                      | Content Type                                     |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| errors.GetCampaignStatusBadRequestError          | 400                                              | application/json                                 |
| errors.GetCampaignStatusUnauthorizedError        | 401                                              | application/json                                 |
| errors.GetCampaignStatusForbiddenError           | 403                                              | application/json                                 |
| errors.GetCampaignStatusNotFoundError            | 404                                              | application/json                                 |
| errors.GetCampaignStatusConflictError            | 409                                              | application/json                                 |
| errors.GetCampaignStatusGoneError                | 410                                              | application/json                                 |
| errors.GetCampaignStatusUnprocessableEntityError | 422                                              | application/json                                 |
| errors.GetCampaignStatusTooManyRequestsError     | 429                                              | application/json                                 |
| errors.GetCampaignStatusInternalServerError      | 500                                              | application/json                                 |
| errors.BereachDefaultError                       | 4XX, 5XX                                         | \*/\*                                            |

## sync

Manually mark actions as completed for profiles within a campaign. Use when actions were performed outside the API (e.g. manual DMs) and need to be synced. 0 credits, no rate limit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="syncCampaignActions" method="post" path="/campaigns/{campaignSlug}/sync" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.campaigns.sync({
    campaignSlug: "<value>",
    body: {
      profiles: [
        {
          profile: "https://www.linkedin.com/in/john-doe",
          actions: [
            "message",
            "reply",
          ],
        },
      ],
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { campaignsSync } from "bereach/funcs/campaigns-sync.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await campaignsSync(bereach, {
    campaignSlug: "<value>",
    body: {
      profiles: [
        {
          profile: "https://www.linkedin.com/in/john-doe",
          actions: [
            "message",
            "reply",
          ],
        },
      ],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("campaignsSync failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.SyncCampaignActionsRequest](../../models/operations/sync-campaign-actions-request.md)                                                                              | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.SyncCampaignActionsResponse](../../models/operations/sync-campaign-actions-response.md)\>**

### Errors

| Error Type                                         | Status Code                                        | Content Type                                       |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| errors.SyncCampaignActionsBadRequestError          | 400                                                | application/json                                   |
| errors.SyncCampaignActionsUnauthorizedError        | 401                                                | application/json                                   |
| errors.SyncCampaignActionsForbiddenError           | 403                                                | application/json                                   |
| errors.SyncCampaignActionsNotFoundError            | 404                                                | application/json                                   |
| errors.SyncCampaignActionsConflictError            | 409                                                | application/json                                   |
| errors.SyncCampaignActionsGoneError                | 410                                                | application/json                                   |
| errors.SyncCampaignActionsUnprocessableEntityError | 422                                                | application/json                                   |
| errors.SyncCampaignActionsTooManyRequestsError     | 429                                                | application/json                                   |
| errors.SyncCampaignActionsInternalServerError      | 500                                                | application/json                                   |
| errors.BereachDefaultError                         | 4XX, 5XX                                           | \*/\*                                              |

## getStats

Returns per-action counts, unique profile count, and total credits used for a campaign. 0 credits, no rate limit.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getCampaignStats" method="post" path="/campaigns/{campaignSlug}/stats" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.campaigns.getStats({
    campaignSlug: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { campaignsGetStats } from "bereach/funcs/campaigns-get-stats.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await campaignsGetStats(bereach, {
    campaignSlug: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("campaignsGetStats failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetCampaignStatsRequest](../../models/operations/get-campaign-stats-request.md)                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetCampaignStatsResponse](../../models/operations/get-campaign-stats-response.md)\>**

### Errors

| Error Type                                      | Status Code                                     | Content Type                                    |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| errors.GetCampaignStatsBadRequestError          | 400                                             | application/json                                |
| errors.GetCampaignStatsUnauthorizedError        | 401                                             | application/json                                |
| errors.GetCampaignStatsForbiddenError           | 403                                             | application/json                                |
| errors.GetCampaignStatsNotFoundError            | 404                                             | application/json                                |
| errors.GetCampaignStatsConflictError            | 409                                             | application/json                                |
| errors.GetCampaignStatsGoneError                | 410                                             | application/json                                |
| errors.GetCampaignStatsUnprocessableEntityError | 422                                             | application/json                                |
| errors.GetCampaignStatsTooManyRequestsError     | 429                                             | application/json                                |
| errors.GetCampaignStatsInternalServerError      | 500                                             | application/json                                |
| errors.BereachDefaultError                      | 4XX, 5XX                                        | \*/\*                                           |
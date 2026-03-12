# Contacts

## Overview

Endpoints for managing contacts and lifecycle stages without requiring a campaign

### Available Operations

* [upsert](#upsert) - Create or upsert contacts (no campaign required)

## upsert

Save contacts organically without creating a campaign first. Upserts by LinkedIn URL — if the contact already exists for this user, it updates the name and optional fields. Returns full contact objects with IDs so the AI agent can immediately log activities and update lifecycle stages.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="upsertContacts" method="post" path="/contacts" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.contacts.upsert({
    contacts: [
      {
        linkedinUrl: "https://linkedin.com/in/johndoe",
        name: "John Doe",
        source: "search_results",
      },
      {
        linkedinUrl: "https://linkedin.com/in/janesmith",
        name: "Jane Smith",
        source: "likes",
        sourceAngle: "competitor-engagement",
        lifecycleStage: "lead",
        hotScore: 75,
      },
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
import { contactsUpsert } from "bereach/funcs/contacts-upsert.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await contactsUpsert(bereach, {
    contacts: [
      {
        linkedinUrl: "https://linkedin.com/in/johndoe",
        name: "John Doe",
        source: "search_results",
      },
      {
        linkedinUrl: "https://linkedin.com/in/janesmith",
        name: "Jane Smith",
        source: "likes",
        sourceAngle: "competitor-engagement",
        lifecycleStage: "lead",
        hotScore: 75,
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("contactsUpsert failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpsertContactsRequest](../../models/operations/upsert-contacts-request.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.UpsertContactsResponse](../../models/operations/upsert-contacts-response.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.BereachDefaultError | 4XX, 5XX                   | \*/\*                      |
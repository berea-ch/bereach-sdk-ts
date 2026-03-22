# Search

## Overview

Search LinkedIn for posts, people, companies, and jobs. Includes parameter resolution (typeahead) for converting text to LinkedIn IDs.

### Available Operations

* [resolveParameters](#resolveparameters) - Resolve text to LinkedIn search parameter IDs (typeahead)

## resolveParameters

# Resolve Search Parameters

Converts human-readable text into LinkedIn numeric IDs required by search filters. This is a **prerequisite step** before using location, industry, company, or school filters in any search endpoint.

## Supported types
| Type | Description | Use with filter |
|------|-------------|------------------|
| `GEO` | Geographic locations (cities, regions, countries) | `location` filter in people, companies, jobs |
| `COMPANY` | Companies and organizations | `currentCompany`, `pastCompany`, `authorCompany` |
| `INDUSTRY` | Industries and sectors | `industry`, `authorIndustry` |
| `SCHOOL` | Schools and universities | `school` filter in people search |
| `CONNECTIONS` | Your LinkedIn connections by name | Identify connection URNs |
| `PEOPLE` | Any LinkedIn user by name | Identify profile URNs for `connectionOf` |

## How to use
```
Step 1: GET /search/linkedin/parameters?type=GEO&keywords=Paris
        → [{ id: '105015875', title: 'Paris, Île-de-France, France', type: 'GEO' }]
Step 2: POST /search/linkedin/people { location: ['105015875'], keywords: 'engineer' }
        → returns engineers in Paris
```

## Response format
Each item contains `id` (the LinkedIn numeric ID to use in filters), `title` (human-readable label), and `type` (the parameter type).

## Tips
- Use short, specific keywords for best results (e.g. `"Paris"` not `"Paris, France"`)
- The API returns up to `limit` results (default 10, max 50)
- Results are ranked by relevance
- IDs are stable — you can cache them for repeated searches

**Note**: This is a GET endpoint. Pass `type`, `keywords`, and `limit` as query parameters.
Example: `GET /search/linkedin/parameters?type=GEO&keywords=Paris&limit=5`

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resolveParameters" method="get" path="/search/linkedin/parameters" -->
```typescript
import { Bereach } from "bereach";

const bereach = new Bereach({
  token: "BEREACH_API_KEY",
});

async function run() {
  const result = await bereach.search.resolveParameters({
    type: "PEOPLE",
    keywords: "<value>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { BereachCore } from "bereach/core.js";
import { searchResolveParameters } from "bereach/funcs/search-resolve-parameters.js";

// Use `BereachCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const bereach = new BereachCore({
  token: "BEREACH_API_KEY",
});

async function run() {
  const res = await searchResolveParameters(bereach, {
    type: "PEOPLE",
    keywords: "<value>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("searchResolveParameters failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResolveParametersRequest](../../models/operations/resolve-parameters-request.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ResolveParametersResponse](../../models/operations/resolve-parameters-response.md)\>**

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
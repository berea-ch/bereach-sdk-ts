# GlobalActivitiesRequest

## Example Usage

```typescript
import { GlobalActivitiesRequest } from "bereach/models/operations";

let value: GlobalActivitiesRequest = {};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `type`                                                                       | *string*                                                                     | :heavy_minus_sign:                                                           | Comma-separated activity types to filter (e.g. 'message,connection_request') |
| `campaignId`                                                                 | *string*                                                                     | :heavy_minus_sign:                                                           | Filter activities to contacts in this campaign                               |
| `from`                                                                       | *string*                                                                     | :heavy_minus_sign:                                                           | ISO date/time lower bound for createdAt                                      |
| `to`                                                                         | *string*                                                                     | :heavy_minus_sign:                                                           | ISO date/time upper bound for createdAt                                      |
| `limit`                                                                      | *number*                                                                     | :heavy_minus_sign:                                                           | Results per page (max 200)                                                   |
| `offset`                                                                     | *number*                                                                     | :heavy_minus_sign:                                                           | Pagination offset                                                            |
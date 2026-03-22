# BulkVisitProfileRequest

## Example Usage

```typescript
import { BulkVisitProfileRequest } from "bereach/models/operations";

let value: BulkVisitProfileRequest = {
  profiles: [
    "<value 1>",
    "<value 2>",
  ],
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `profiles`                                                                                     | *string*[]                                                                                     | :heavy_check_mark:                                                                             | LinkedIn profile URLs, vanity names, or URNs (max 50). Duplicates are auto-removed.            |
| `campaignSlug`                                                                                 | *string*                                                                                       | :heavy_minus_sign:                                                                             | Auto-add each successfully visited contact to this campaign.                                   |
| `includePosts`                                                                                 | *boolean*                                                                                      | :heavy_minus_sign:                                                                             | Fetch last 5 posts per profile. Increases processing time.                                     |
| `includeComments`                                                                              | *boolean*                                                                                      | :heavy_minus_sign:                                                                             | Fetch recent comments per profile. Increases processing time.                                  |
| `includeAbout`                                                                                 | *boolean*                                                                                      | :heavy_minus_sign:                                                                             | Fetch About section and detailed position descriptions per profile. Increases processing time. |
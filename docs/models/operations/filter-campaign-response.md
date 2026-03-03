# FilterCampaignResponse

Filter status with checked slugs

## Example Usage

```typescript
import { FilterCampaignResponse } from "bereach/models/operations";

let value: FilterCampaignResponse = {
  filtered: true,
  checkedSlugs: [],
  creditsUsed: 573489,
  retryAfter: 798143,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `filtered`                                                                                            | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | True if all actionSlugs have been completed for this campaign, meaning the entire flow can be skipped |
| `checkedSlugs`                                                                                        | [operations.CheckedSlug](../../models/operations/checked-slug.md)[]                                   | :heavy_check_mark:                                                                                    | Status of each action slug — completed means the action was already executed for this campaign        |
| `creditsUsed`                                                                                         | *number*                                                                                              | :heavy_check_mark:                                                                                    | Credits consumed by this call (always 0 for campaign queries).                                        |
| `retryAfter`                                                                                          | *number*                                                                                              | :heavy_check_mark:                                                                                    | Seconds to wait before next call of the same type (always 0 for campaign queries).                    |
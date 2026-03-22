# FilterRequest

## Example Usage

```typescript
import { FilterRequest } from "bereach/models/operations";

let value: FilterRequest = {
  campaignSlug: "<value>",
  actionSlugs: "<value>",
};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `campaignSlug`                                                                                         | *string*                                                                                               | :heavy_check_mark:                                                                                     | Unique identifier for the automation campaign (e.g., 'lead-magnet-post-12345', 'outreach-webinar-feb') |
| `actionSlugs`                                                                                          | *string*                                                                                               | :heavy_check_mark:                                                                                     | Comma-separated list of action slugs to check (e.g., 'send-mp-john-doe,like-comment-abc123')           |
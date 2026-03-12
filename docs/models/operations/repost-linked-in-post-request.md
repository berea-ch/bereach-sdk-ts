# RepostLinkedInPostRequest

## Example Usage

```typescript
import { RepostLinkedInPostRequest } from "bereach/models/operations";

let value: RepostLinkedInPostRequest = {
  postUrl: "https://bad-bookcase.net",
  text: "<value>",
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `postUrl`                                        | *string*                                         | :heavy_check_mark:                               | LinkedIn post URL to repost                      |
| `text`                                           | *string*                                         | :heavy_check_mark:                               | Quote text for the repost (required by LinkedIn) |
| `campaignSlug`                                   | *string*                                         | :heavy_minus_sign:                               | Campaign identifier for deduplication            |
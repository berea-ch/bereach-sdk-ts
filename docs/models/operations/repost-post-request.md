# RepostPostRequest

## Example Usage

```typescript
import { RepostPostRequest } from "bereach/models/operations";

let value: RepostPostRequest = {
  postUrl: "https://zealous-runway.name",
  text: "<value>",
};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `postUrl`                                        | *string*                                         | :heavy_check_mark:                               | LinkedIn post URL to repost                      |
| `text`                                           | *string*                                         | :heavy_check_mark:                               | Quote text for the repost (required by LinkedIn) |
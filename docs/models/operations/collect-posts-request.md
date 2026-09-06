# CollectPostsRequest

## Example Usage

```typescript
import { CollectPostsRequest } from "bereach/models/operations";

let value: CollectPostsRequest = {
  profileUrl: "https://nifty-onset.com/",
};
```

## Fields

| Field                                                                                                                                                 | Type                                                                                                                                                  | Required                                                                                                                                              | Description                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| `profileUrl`                                                                                                                                          | *string*                                                                                                                                              | :heavy_check_mark:                                                                                                                                    | LinkedIn profile or company page URL, vanity name, or URN. Company URLs use the organization feed; personal URLs use the profile activity feed.       |
| `more`                                                                                                                                                | *boolean*                                                                                                                                             | :heavy_minus_sign:                                                                                                                                    | Next page of the same profile. Set only when the user asked for more posts or tapped Load more. Each page uses the connected account's action budget. |
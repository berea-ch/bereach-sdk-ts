# PublicPostEngagersRequest

## Example Usage

```typescript
import { PublicPostEngagersRequest } from "bereach/models/operations";

let value: PublicPostEngagersRequest = {
  postUrl: "https://incomplete-planula.net/",
};
```

## Fields

| Field                                                                                                                      | Type                                                                                                                       | Required                                                                                                                   | Description                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `postUrl`                                                                                                                  | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | Full public post URL.                                                                                                      |
| `country`                                                                                                                  | *string*                                                                                                                   | :heavy_minus_sign:                                                                                                         | ISO alpha-2 country code for the proxy exit.                                                                               |
| `save`                                                                                                                     | *boolean*                                                                                                                  | :heavy_minus_sign:                                                                                                         | When true, surfaced commenters are saved to your contacts.                                                                 |
| `hydrate`                                                                                                                  | *boolean*                                                                                                                  | :heavy_minus_sign:                                                                                                         | When true, each commenter's public profile is also fetched to enrich headline, company, and location. Costs extra fetches. |
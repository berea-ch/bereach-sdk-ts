# PublicProfileRequest

## Example Usage

```typescript
import { PublicProfileRequest } from "bereach/models/operations";

let value: PublicProfileRequest = {};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `profileUrl`                                              | *string*                                                  | :heavy_minus_sign:                                        | Full public profile URL. Provide this or slug.            |
| `slug`                                                    | *string*                                                  | :heavy_minus_sign:                                        | Profile vanity slug. Provide this or profileUrl.          |
| `country`                                                 | *string*                                                  | :heavy_minus_sign:                                        | ISO alpha-2 country of the person, when known.            |
| `save`                                                    | *boolean*                                                 | :heavy_minus_sign:                                        | When true, the fetched profile is saved to your contacts. |
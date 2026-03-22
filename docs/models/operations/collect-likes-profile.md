# CollectLikesProfile

## Example Usage

```typescript
import { CollectLikesProfile } from "bereach/models/operations";

let value: CollectLikesProfile = {
  name: "<value>",
  headline: "<value>",
  profileUrl: "https://leading-shadowbox.name/",
  imageUrl: "https://failing-hyphenation.info",
  publicIdentifier: "<value>",
  profileUrn: "<value>",
  type: "like",
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `name`                                                                                     | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `headline`                                                                                 | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `profileUrl`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `imageUrl`                                                                                 | *string*                                                                                   | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `publicIdentifier`                                                                         | *string*                                                                                   | :heavy_check_mark:                                                                         | Vanity slug from profile URL (e.g. john-doe) when not URN-based                            |
| `profileUrn`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                    |
| `type`                                                                                     | [operations.CollectLikesType](../../models/operations/collect-likes-type.md)               | :heavy_check_mark:                                                                         | N/A                                                                                        |
| `reactionType`                                                                             | *string*                                                                                   | :heavy_minus_sign:                                                                         | Reaction type (e.g. 'LIKE', 'CELEBRATE', 'EMPATHY', 'INTEREST', 'PRAISE', 'APPRECIATION'). |
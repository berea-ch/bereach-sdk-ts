# SearchLinkedInItemsPeople

## Example Usage

```typescript
import { SearchLinkedInItemsPeople } from "bereach/models/operations";

let value: SearchLinkedInItemsPeople = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://miserable-fork.name/",
  headline: null,
  location: "<value>",
  profilePicture: "<value>",
  networkDistance: "DISTANCE_3",
  currentPositions: [],
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                     | [operations.SearchLinkedInTypePeople](../../models/operations/search-linked-in-type-people.md)             | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `name`                                                                                                     | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `profileUrl`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `headline`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `location`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `profilePicture`                                                                                           | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `networkDistance`                                                                                          | [operations.SearchLinkedInNetworkDistance](../../models/operations/search-linked-in-network-distance.md)   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `currentPositions`                                                                                         | [operations.SearchLinkedInCurrentPosition](../../models/operations/search-linked-in-current-position.md)[] | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `profileUrn`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                                    |
| `publicIdentifier`                                                                                         | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Vanity slug from profile URL (e.g. john-doe) when not URN-based                                            |
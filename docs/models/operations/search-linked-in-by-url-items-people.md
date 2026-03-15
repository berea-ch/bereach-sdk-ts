# SearchLinkedInByUrlItemsPeople

## Example Usage

```typescript
import { SearchLinkedInByUrlItemsPeople } from "bereach/models/operations";

let value: SearchLinkedInByUrlItemsPeople = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://idealistic-programme.net",
  headline: "<value>",
  location: "<value>",
  profilePicture: "<value>",
  networkDistance: null,
  currentPositions: [],
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                 | [operations.SearchLinkedInByUrlTypePeople](../../models/operations/search-linked-in-by-url-type-people.md)             | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `name`                                                                                                                 | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `profileUrl`                                                                                                           | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `headline`                                                                                                             | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `location`                                                                                                             | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `profilePicture`                                                                                                       | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `networkDistance`                                                                                                      | [operations.SearchLinkedInByUrlNetworkDistance](../../models/operations/search-linked-in-by-url-network-distance.md)   | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `currentPositions`                                                                                                     | [operations.SearchLinkedInByUrlCurrentPosition](../../models/operations/search-linked-in-by-url-current-position.md)[] | :heavy_check_mark:                                                                                                     | N/A                                                                                                                    |
| `profileUrn`                                                                                                           | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                                                |
| `publicIdentifier`                                                                                                     | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | Vanity slug from profile URL (e.g. john-doe) when not URN-based                                                        |
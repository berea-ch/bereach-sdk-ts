# SearchByUrlItemsPeople

## Example Usage

```typescript
import { SearchByUrlItemsPeople } from "bereach/models/operations";

let value: SearchByUrlItemsPeople = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://uneven-castanet.info",
  headline: "<value>",
  location: "<value>",
  profilePicture: "<value>",
  networkDistance: "DISTANCE_1",
  currentPositions: [],
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `type`                                                                                               | [operations.SearchByUrlTypePeople](../../models/operations/search-by-url-type-people.md)             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `name`                                                                                               | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `profileUrl`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `headline`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `location`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `profilePicture`                                                                                     | *string*                                                                                             | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `networkDistance`                                                                                    | [operations.SearchByUrlNetworkDistance](../../models/operations/search-by-url-network-distance.md)   | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `currentPositions`                                                                                   | [operations.SearchByUrlCurrentPosition](../../models/operations/search-by-url-current-position.md)[] | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `profileUrn`                                                                                         | *string*                                                                                             | :heavy_check_mark:                                                                                   | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                              |
| `publicIdentifier`                                                                                   | *string*                                                                                             | :heavy_check_mark:                                                                                   | Vanity slug from profile URL (e.g. john-doe) when not URN-based                                      |
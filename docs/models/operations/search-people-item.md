# SearchPeopleItem

## Example Usage

```typescript
import { SearchPeopleItem } from "bereach/models/operations";

let value: SearchPeopleItem = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://heartfelt-deck.org",
  headline: "<value>",
  location: "<value>",
  profilePicture: "<value>",
  networkDistance: "DISTANCE_1",
  currentPositions: [
    {
      company: "Bernier, Abbott and Feest",
      role: "<value>",
    },
  ],
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `type`                                                                                                | [operations.SearchPeopleType](../../models/operations/search-people-type.md)                          | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `name`                                                                                                | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profileUrl`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `headline`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `location`                                                                                            | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profilePicture`                                                                                      | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `networkDistance`                                                                                     | [operations.SearchPeopleNetworkDistance](../../models/operations/search-people-network-distance.md)   | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `currentPositions`                                                                                    | [operations.SearchPeopleCurrentPosition](../../models/operations/search-people-current-position.md)[] | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `profileUrn`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                               |
| `publicIdentifier`                                                                                    | *string*                                                                                              | :heavy_check_mark:                                                                                    | Vanity slug from profile URL (e.g. john-doe) when not URN-based                                       |
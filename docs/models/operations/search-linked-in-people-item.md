# SearchLinkedInPeopleItem

## Example Usage

```typescript
import { SearchLinkedInPeopleItem } from "bereach/models/operations";

let value: SearchLinkedInPeopleItem = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://tame-birdcage.com/",
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

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                  | [operations.SearchLinkedInPeopleType](../../models/operations/search-linked-in-people-type.md)                          | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `name`                                                                                                                  | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `profileUrl`                                                                                                            | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `headline`                                                                                                              | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `location`                                                                                                              | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `profilePicture`                                                                                                        | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `networkDistance`                                                                                                       | [operations.SearchLinkedInPeopleNetworkDistance](../../models/operations/search-linked-in-people-network-distance.md)   | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `currentPositions`                                                                                                      | [operations.SearchLinkedInPeopleCurrentPosition](../../models/operations/search-linked-in-people-current-position.md)[] | :heavy_check_mark:                                                                                                      | N/A                                                                                                                     |
| `profileUrn`                                                                                                            | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                                                 |
| `publicIdentifier`                                                                                                      | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | Vanity slug from profile URL (e.g. john-doe) when not URN-based                                                         |
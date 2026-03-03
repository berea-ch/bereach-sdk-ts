# SearchLinkedInItemsPeople

## Example Usage

```typescript
import { SearchLinkedInItemsPeople } from "bereach/models/operations";

let value: SearchLinkedInItemsPeople = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://glossy-legging.info",
  headline: "<value>",
  location: null,
  profilePicture: "<value>",
  networkDistance: "OUT_OF_NETWORK",
  currentPositions: [
    {
      company: "Hane - Stanton",
      role: "<value>",
    },
  ],
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
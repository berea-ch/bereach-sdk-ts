# ItemsPeople

## Example Usage

```typescript
import { ItemsPeople } from "bereach/models/operations";

let value: ItemsPeople = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://teeming-earth.net/",
  headline: "<value>",
  location: "<value>",
  profilePicture: null,
  networkDistance: "DISTANCE_3",
  currentPositions: [
    {
      company: "Hagenes, Padberg and Hayes",
      role: "<value>",
    },
  ],
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `type`                                                                                 | [operations.ItemsTypePeople](../../models/operations/items-type-people.md)             | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `name`                                                                                 | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `profileUrl`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `headline`                                                                             | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `location`                                                                             | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `profilePicture`                                                                       | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `networkDistance`                                                                      | [operations.ItemsNetworkDistance](../../models/operations/items-network-distance.md)   | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `currentPositions`                                                                     | [operations.ItemsCurrentPosition](../../models/operations/items-current-position.md)[] | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `profileUrn`                                                                           | *string*                                                                               | :heavy_check_mark:                                                                     | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available                |
| `publicIdentifier`                                                                     | *string*                                                                               | :heavy_check_mark:                                                                     | Vanity slug from profile URL (e.g. john-doe) when not URN-based                        |
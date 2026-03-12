# SearchSalesNavItemPeople

## Example Usage

```typescript
import { SearchSalesNavItemPeople } from "bereach/models/operations";

let value: SearchSalesNavItemPeople = {
  type: "PEOPLE",
  id: "<id>",
  name: "<value>",
  firstName: "Maeve",
  lastName: "Adams",
  memberUrn: "<value>",
  publicIdentifier: "<value>",
  profileUrl: "https://bulky-corporation.biz/",
  salesNavUrl: null,
  profilePicture: null,
  headline: "<value>",
  location: "<value>",
  networkDistance: "DISTANCE_3",
  premium: true,
  openProfile: null,
  pendingInvitation: true,
  currentPositions: [
    {
      company: "Yundt - Tromp",
      companyId: "<id>",
      role: "<value>",
      description: "yippee pigsty while black why",
      location: null,
      tenureAtCompany: {},
      tenureAtRole: {},
    },
  ],
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                     | [operations.SearchSalesNavTypePeople](../../models/operations/search-sales-nav-type-people.md)             | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `id`                                                                                                       | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Sales Navigator lead ID                                                                                    |
| `name`                                                                                                     | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `firstName`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `lastName`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `memberUrn`                                                                                                | *string*                                                                                                   | :heavy_check_mark:                                                                                         | LinkedIn member URN (e.g. urn:li:member:12345)                                                             |
| `publicIdentifier`                                                                                         | *string*                                                                                                   | :heavy_check_mark:                                                                                         | LinkedIn vanity URL slug                                                                                   |
| `profileUrl`                                                                                               | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Public LinkedIn profile URL                                                                                |
| `salesNavUrl`                                                                                              | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Sales Navigator lead URL                                                                                   |
| `profilePicture`                                                                                           | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `headline`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `location`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `networkDistance`                                                                                          | [operations.SearchSalesNavNetworkDistance](../../models/operations/search-sales-nav-network-distance.md)   | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `premium`                                                                                                  | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `openProfile`                                                                                              | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `pendingInvitation`                                                                                        | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `currentPositions`                                                                                         | [operations.SearchSalesNavCurrentPosition](../../models/operations/search-sales-nav-current-position.md)[] | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
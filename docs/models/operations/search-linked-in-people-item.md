# SearchLinkedInPeopleItem

## Example Usage

```typescript
import { SearchLinkedInPeopleItem } from "bereach/models/operations";

let value: SearchLinkedInPeopleItem = {
  type: "PEOPLE",
  name: "<value>",
  profileUrl: "https://amazing-soybean.com",
  headline: "<value>",
  location: "<value>",
  profilePicture: "<value>",
  networkDistance: "OUT_OF_NETWORK",
  currentPositions: [],
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
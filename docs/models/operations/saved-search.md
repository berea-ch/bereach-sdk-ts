# SavedSearch

## Example Usage

```typescript
import { SavedSearch } from "bereach/models/operations";

let value: SavedSearch = {
  id: "<id>",
  name: "<value>",
  category: "people",
  savedSearchUrl: "https://likable-marten.info/",
  newResultsCount: 60649,
  lastUsedAt: "<value>",
};
```

## Fields

| Field                                                                                                             | Type                                                                                                              | Required                                                                                                          | Description                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                              | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `name`                                                                                                            | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `category`                                                                                                        | [operations.ListSalesNavSavedSearchesCategory](../../models/operations/list-sales-nav-saved-searches-category.md) | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
| `savedSearchUrl`                                                                                                  | *string*                                                                                                          | :heavy_check_mark:                                                                                                | Full Sales Navigator search URL — pass straight into search_sales_nav_people/companies via the `url` field.       |
| `newResultsCount`                                                                                                 | *number*                                                                                                          | :heavy_check_mark:                                                                                                | New matches since the user last viewed this saved search, if LinkedIn reports it.                                 |
| `lastUsedAt`                                                                                                      | *string*                                                                                                          | :heavy_check_mark:                                                                                                | N/A                                                                                                               |
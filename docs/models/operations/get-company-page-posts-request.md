# GetCompanyPagePostsRequest

## Example Usage

```typescript
import { GetCompanyPagePostsRequest } from "bereach/models/operations";

let value: GetCompanyPagePostsRequest = {
  universalName: "<value>",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `universalName`                                                               | *string*                                                                      | :heavy_check_mark:                                                            | Company URL slug (e.g. 'openai'). Same value as returned by listCompanyPages. |
| `count`                                                                       | *number*                                                                      | :heavy_minus_sign:                                                            | Number of posts to return (max 50).                                           |
| `start`                                                                       | *number*                                                                      | :heavy_minus_sign:                                                            | Pagination offset.                                                            |
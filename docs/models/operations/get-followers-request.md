# GetFollowersRequest

## Example Usage

```typescript
import { GetFollowersRequest } from "bereach/models/operations";

let value: GetFollowersRequest = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `start`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Pagination offset (default 0).                              |
| `count`                                                     | *number*                                                    | :heavy_minus_sign:                                          | Number of followers to fetch per page (default 10, max 50). |
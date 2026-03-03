# Follower

## Example Usage

```typescript
import { Follower } from "bereach/models/operations";

let value: Follower = {
  name: "<value>",
  headline: null,
  profileUrl: "https://junior-secrecy.biz",
  profilePicture: null,
  followerCount: 871561,
  following: false,
};
```

## Fields

| Field                               | Type                                | Required                            | Description                         |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `name`                              | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `headline`                          | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `profileUrl`                        | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `profilePicture`                    | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `followerCount`                     | *number*                            | :heavy_check_mark:                  | N/A                                 |
| `following`                         | *boolean*                           | :heavy_check_mark:                  | Whether you follow this person back |
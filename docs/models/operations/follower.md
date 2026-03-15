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
  profileUrn: "<value>",
  publicIdentifier: "<value>",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `name`                                                                  | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `headline`                                                              | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `profileUrl`                                                            | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `profilePicture`                                                        | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `followerCount`                                                         | *number*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `following`                                                             | *boolean*                                                               | :heavy_check_mark:                                                      | Whether you follow this person back                                     |
| `profileUrn`                                                            | *string*                                                                | :heavy_check_mark:                                                      | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available |
| `publicIdentifier`                                                      | *string*                                                                | :heavy_check_mark:                                                      | Vanity slug from profile URL (e.g. john-doe) when not URN-based         |
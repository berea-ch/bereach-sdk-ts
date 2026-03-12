# GetMyLinkedInProfileResponse

Stored LinkedIn profile data

## Example Usage

```typescript
import { GetMyLinkedInProfileResponse } from "bereach/models/operations";

let value: GetMyLinkedInProfileResponse = {
  success: true,
  linkedinProfileId: "<id>",
  linkedinName: "<value>",
  linkedinEmail: "<value>",
  profileUrn: "<value>",
  headline: "<value>",
  profilePic: null,
  profileUrl: null,
  connectionsCount: 200599,
  location: {
    countryCode: "LC",
  },
  isVerified: false,
  creditsUsed: 466283,
  retryAfter: 477405,
};
```

## Fields

| Field                                                                                                       | Type                                                                                                        | Required                                                                                                    | Description                                                                                                 |
| ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                   | *true*                                                                                                      | :heavy_check_mark:                                                                                          | N/A                                                                                                         |
| `linkedinProfileId`                                                                                         | *string*                                                                                                    | :heavy_check_mark:                                                                                          | LinkedIn vanity name (e.g., 'alexandre-sarfati')                                                            |
| `linkedinName`                                                                                              | *string*                                                                                                    | :heavy_check_mark:                                                                                          | Full name from LinkedIn                                                                                     |
| `linkedinEmail`                                                                                             | *string*                                                                                                    | :heavy_check_mark:                                                                                          | Email from LinkedIn profile                                                                                 |
| `profileUrn`                                                                                                | *string*                                                                                                    | :heavy_check_mark:                                                                                          | LinkedIn profile URN                                                                                        |
| `headline`                                                                                                  | *string*                                                                                                    | :heavy_check_mark:                                                                                          | LinkedIn headline                                                                                           |
| `profilePic`                                                                                                | *string*                                                                                                    | :heavy_check_mark:                                                                                          | Profile picture URL                                                                                         |
| `profileUrl`                                                                                                | *string*                                                                                                    | :heavy_check_mark:                                                                                          | Full LinkedIn profile URL                                                                                   |
| `positions`                                                                                                 | [operations.GetMyLinkedInProfilePosition](../../models/operations/get-my-linked-in-profile-position.md)[]   | :heavy_minus_sign:                                                                                          | Work positions (populated after /refresh)                                                                   |
| `educations`                                                                                                | [operations.GetMyLinkedInProfileEducation](../../models/operations/get-my-linked-in-profile-education.md)[] | :heavy_minus_sign:                                                                                          | Education entries (populated after /refresh)                                                                |
| `connectionsCount`                                                                                          | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Total LinkedIn connections                                                                                  |
| `location`                                                                                                  | [operations.GetMyLinkedInProfileLocation](../../models/operations/get-my-linked-in-profile-location.md)     | :heavy_check_mark:                                                                                          | Profile location                                                                                            |
| `isVerified`                                                                                                | *boolean*                                                                                                   | :heavy_check_mark:                                                                                          | LinkedIn verification status                                                                                |
| `lastPosts`                                                                                                 | [operations.GetMyLinkedInProfileLastPost](../../models/operations/get-my-linked-in-profile-last-post.md)[]  | :heavy_minus_sign:                                                                                          | Last 5 posts (populated when posts have been fetched via /me/linkedin/posts)                                |
| `creditsUsed`                                                                                               | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Credits consumed by this call (0 for free endpoints, cached results, or duplicates).                        |
| `retryAfter`                                                                                                | *number*                                                                                                    | :heavy_check_mark:                                                                                          | Seconds to wait before making another call of the same type. 0 means no wait needed.                        |
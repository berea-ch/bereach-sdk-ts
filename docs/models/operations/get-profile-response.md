# GetProfileResponse

Stored LinkedIn profile data

## Example Usage

```typescript
import { GetProfileResponse } from "bereach/models/operations";

let value: GetProfileResponse = {
  success: true,
  linkedinProfileId: "<id>",
  linkedinName: "<value>",
  linkedinEmail: "<value>",
  profileUrn: "<value>",
  headline: "<value>",
  profilePic: "<value>",
  profileUrl: "https://odd-alliance.net/",
  connectionsCount: 917540,
  location: {
    countryCode: "SX",
  },
  isVerified: true,
  creditsUsed: 55690,
  retryAfter: 22380,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `linkedinProfileId`                                                                  | *string*                                                                             | :heavy_check_mark:                                                                   | LinkedIn vanity name (e.g., 'alexandre-sarfati')                                     |
| `linkedinName`                                                                       | *string*                                                                             | :heavy_check_mark:                                                                   | Full name from LinkedIn                                                              |
| `linkedinEmail`                                                                      | *string*                                                                             | :heavy_check_mark:                                                                   | Email from LinkedIn profile                                                          |
| `profileUrn`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | LinkedIn profile URN                                                                 |
| `headline`                                                                           | *string*                                                                             | :heavy_check_mark:                                                                   | LinkedIn headline                                                                    |
| `profilePic`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | Profile picture URL                                                                  |
| `profileUrl`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | Full LinkedIn profile URL                                                            |
| `summary`                                                                            | *string*                                                                             | :heavy_minus_sign:                                                                   | About section text (populated after /refresh with includeAbout)                      |
| `positions`                                                                          | [operations.GetProfilePosition](../../models/operations/get-profile-position.md)[]   | :heavy_minus_sign:                                                                   | Work positions (populated after /refresh)                                            |
| `educations`                                                                         | [operations.GetProfileEducation](../../models/operations/get-profile-education.md)[] | :heavy_minus_sign:                                                                   | Education entries (populated after /refresh)                                         |
| `connectionsCount`                                                                   | *number*                                                                             | :heavy_check_mark:                                                                   | Total LinkedIn connections                                                           |
| `location`                                                                           | [operations.GetProfileLocation](../../models/operations/get-profile-location.md)     | :heavy_check_mark:                                                                   | Profile location                                                                     |
| `isVerified`                                                                         | *boolean*                                                                            | :heavy_check_mark:                                                                   | LinkedIn verification status                                                         |
| `lastPosts`                                                                          | [operations.GetProfileLastPost](../../models/operations/get-profile-last-post.md)[]  | :heavy_minus_sign:                                                                   | Last 5 posts (populated when posts have been fetched via /me/linkedin/posts)         |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |
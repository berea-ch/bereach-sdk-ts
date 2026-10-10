# GetRecommendedPeoplePerson

## Example Usage

```typescript
import { GetRecommendedPeoplePerson } from "bereach/models/operations";

let value: GetRecommendedPeoplePerson = {
  name: "<value>",
  headline: "<value>",
  profileUrl: null,
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  profilePicture: "<value>",
  insight: "<value>",
  connectionDegree: null,
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `name`                                                                                                             | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `headline`                                                                                                         | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `profileUrl`                                                                                                       | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `profileUrn`                                                                                                       | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `publicIdentifier`                                                                                                 | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |
| `profilePicture`                                                                                                   | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | Profile picture URL                                                                                                |
| `insight`                                                                                                          | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | The reason LinkedIn gives for suggesting this person, in its own words. Null when it gave none, which is ordinary. |
| `connectionDegree`                                                                                                 | *null*                                                                                                             | :heavy_check_mark:                                                                                                 | Always null. These people are not connections and LinkedIn does not say how far away they are.                     |
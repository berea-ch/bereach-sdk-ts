# UnfollowLinkedInProfileRequest

## Example Usage

```typescript
import { UnfollowLinkedInProfileRequest } from "bereach/models/operations";

let value: UnfollowLinkedInProfileRequest = {
  profile: "<value>",
};
```

## Fields

| Field                                                                                                                                                  | Type                                                                                                                                                   | Required                                                                                                                                               | Description                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `profile`                                                                                                                                              | *string*                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | Accepts full LinkedIn profile URLs (e.g. linkedin.com/in/username), vanity names (e.g. john-doe), or profile URNs (e.g. urn:li:fsd_profile:ACoAAA...). |
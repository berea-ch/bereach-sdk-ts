# PublicProfileResponse

Public profile data

## Example Usage

```typescript
import { PublicProfileResponse } from "bereach/models/operations";

let value: PublicProfileResponse = {
  source: "public",
  completeness: "<value>",
  saved: true,
  profile: {
    "key": "<value>",
    "key1": "<value>",
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `source`                                                                           | [operations.PublicProfileSource](../../models/operations/public-profile-source.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `completeness`                                                                     | *string*                                                                           | :heavy_check_mark:                                                                 | How complete the fetched public profile is.                                        |
| `saved`                                                                            | *boolean*                                                                          | :heavy_check_mark:                                                                 | Whether the profile was saved to your contacts.                                    |
| `profile`                                                                          | Record<string, *any*>                                                              | :heavy_check_mark:                                                                 | The public profile data.                                                           |
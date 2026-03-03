# ConnectLinkedInProfileRequest

## Example Usage

```typescript
import { ConnectLinkedInProfileRequest } from "bereach/models/operations";

let value: ConnectLinkedInProfileRequest = {
  profile: "<value>",
};
```

## Fields

| Field                                                                                                                                                       | Type                                                                                                                                                        | Required                                                                                                                                                    | Description                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `profile`                                                                                                                                                   | *string*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | LinkedIn profile URL (e.g., 'https://www.linkedin.com/in/username') or profile URN (e.g., 'urn:li:fsd_profile:ACoAABZ0Qo4B6pt58d4FVmts1F7TPi4D1-uL1fw')     |
| `campaignSlug`                                                                                                                                              | *string*                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                          | Campaign identifier for deduplication. Dedup by profile automatically.                                                                                      |
| ~~`actionSlug`~~                                                                                                                                            | *string*                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                          | : warning: ** DEPRECATED **: This will be removed in a future release, please migrate away from it as soon as possible.<br/><br/>Deprecated. Use campaignSlug only. |
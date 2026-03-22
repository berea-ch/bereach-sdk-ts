# Connection

## Example Usage

```typescript
import { Connection } from "bereach/models/operations";

let value: Connection = {
  name: "<value>",
  headline: "<value>",
  profileUrl: "https://strong-mom.net/",
  imageUrl: "https://helpful-commodity.info",
  publicIdentifier: "<value>",
  profileUrn: "<value>",
  connectedAt: "<value>",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `name`                                                                  | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `headline`                                                              | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `profileUrl`                                                            | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `imageUrl`                                                              | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
| `publicIdentifier`                                                      | *string*                                                                | :heavy_check_mark:                                                      | Vanity slug from profile URL (e.g. john-doe) when not URN-based         |
| `profileUrn`                                                            | *string*                                                                | :heavy_check_mark:                                                      | LinkedIn profile URN (e.g. urn:li:fsd_profile:ACoAAA...) when available |
| `connectedAt`                                                           | *string*                                                                | :heavy_check_mark:                                                      | N/A                                                                     |
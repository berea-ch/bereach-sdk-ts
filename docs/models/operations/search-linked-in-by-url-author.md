# SearchLinkedInByUrlAuthor

## Example Usage

```typescript
import { SearchLinkedInByUrlAuthor } from "bereach/models/operations";

let value: SearchLinkedInByUrlAuthor = {
  name: "<value>",
  profileUrl: "https://warm-cinder.net",
  headline: null,
  profilePicture: "<value>",
  isCompany: true,
  publicIdentifier: "<value>",
  profileUrn: "<value>",
};
```

## Fields

| Field                               | Type                                | Required                            | Description                         |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `name`                              | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `profileUrl`                        | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `headline`                          | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `profilePicture`                    | *string*                            | :heavy_check_mark:                  | N/A                                 |
| `isCompany`                         | *boolean*                           | :heavy_check_mark:                  | N/A                                 |
| `publicIdentifier`                  | *string*                            | :heavy_check_mark:                  | Vanity slug when not URN-based      |
| `profileUrn`                        | *string*                            | :heavy_check_mark:                  | LinkedIn profile URN when available |
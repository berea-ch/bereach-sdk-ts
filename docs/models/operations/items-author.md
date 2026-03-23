# ItemsAuthor

## Example Usage

```typescript
import { ItemsAuthor } from "bereach/models/operations";

let value: ItemsAuthor = {
  name: "<value>",
  profileUrl: "https://small-provision.com",
  headline: "<value>",
  profilePicture: "<value>",
  isCompany: false,
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
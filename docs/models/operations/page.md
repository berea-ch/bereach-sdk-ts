# Page

## Example Usage

```typescript
import { Page } from "bereach/models/operations";

let value: Page = {
  id: "<id>",
  universalName: "<value>",
  name: "<value>",
  url: "https://quick-witted-disk.info/",
  logoUrl: "https://simplistic-monster.org/",
  followerCount: 5365.52,
  industry: "<value>",
  employeeCount: 7192.61,
  adminRole: "<value>",
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `id`                                                                         | *string*                                                                     | :heavy_check_mark:                                                           | LinkedIn numeric company ID.                                                 |
| `universalName`                                                              | *string*                                                                     | :heavy_check_mark:                                                           | Company URL slug (e.g. 'openai').                                            |
| `name`                                                                       | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `url`                                                                        | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `logoUrl`                                                                    | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `followerCount`                                                              | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `industry`                                                                   | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `employeeCount`                                                              | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `adminRole`                                                                  | *string*                                                                     | :heavy_check_mark:                                                           | Admin role (e.g. 'ADMINISTRATOR', 'CONTENT_ADMIN'). Null if role is unknown. |
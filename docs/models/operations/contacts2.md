# Contacts2

Identity and verdict only. No profile blob, no campaign membership, no timestamps.

## Example Usage

```typescript
import { Contacts2 } from "bereach/models/operations";

let value: Contacts2 = {
  id: "<id>",
  linkedinUrl: "https://ironclad-metal.net/",
  name: "<value>",
  lifecycleStage: "<value>",
  hotScore: 585483,
  outreachStatus: "<value>",
  doNotContact: true,
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `linkedinUrl`                                          | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `name`                                                 | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `lifecycleStage`                                       | *string*                                               | :heavy_check_mark:                                     | Optional Fit label, or ungraded when the row has none. |
| `hotScore`                                             | *number*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `outreachStatus`                                       | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `doNotContact`                                         | *boolean*                                              | :heavy_check_mark:                                     | N/A                                                    |
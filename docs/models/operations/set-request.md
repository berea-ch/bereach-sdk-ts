# SetRequest

## Example Usage

```typescript
import { SetRequest } from "bereach/models/operations";

let value: SetRequest = {
  type: "<value>",
  content: "<value>",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `type`                                                                                             | *string*                                                                                           | :heavy_check_mark:                                                                                 | Context type: "user-profile", "product-pitch", "icp", "tone-voice", "playbook", or "custom:{slug}" |
| `content`                                                                                          | *string*                                                                                           | :heavy_check_mark:                                                                                 | Markdown content                                                                                   |
| `scope`                                                                                            | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Defaults to "user"                                                                                 |
| `label`                                                                                            | *string*                                                                                           | :heavy_minus_sign:                                                                                 | Display label                                                                                      |
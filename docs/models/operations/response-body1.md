# ResponseBody1

## Example Usage

```typescript
import { ResponseBody1 } from "bereach/models/operations";

let value: ResponseBody1 = {
  success: true,
  invite: {
    id: "<id>",
    email: "Ellis48@hotmail.com",
    name: null,
    code: "<value>",
    maxUses: 949705,
    useCount: 867079,
    expiresAt: "1745675942128",
    createdAt: "1732496019313",
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `success`                                                | *true*                                                   | :heavy_check_mark:                                       | N/A                                                      |
| `invite`                                                 | [operations.Invite1](../../models/operations/invite1.md) | :heavy_check_mark:                                       | N/A                                                      |
# EditPostMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { EditPostMeta } from "bereach/models/operations";

let value: EditPostMeta = {
  credits: {
    current: 468.67,
    limit: 391.47,
    remaining: 8814.49,
    percentage: 297.88,
    isUnlimited: false,
  },
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `credits`                                                                  | [operations.EditPostCredits](../../models/operations/edit-post-credits.md) | :heavy_check_mark:                                                         | N/A                                                                        |
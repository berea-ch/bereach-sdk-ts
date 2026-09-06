# UpcomingWhy

Why this person has not gone out yet, as the sender itself answers it. A block on the account outranks the place in line.

## Example Usage

```typescript
import { UpcomingWhy } from "bereach/models/operations";

let value: UpcomingWhy = {
  status: "blocked",
  detail: "<value>",
  clearsItself: false,
  fixUrl: "https://pricey-fun.info",
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `status`                                                                                                   | [operations.UpcomingStatus](../../models/operations/upcoming-status.md)                                    | :heavy_check_mark:                                                                                         | next is first in line, not sent; waiting names the place; blocked carries the account's own sentence.      |
| `detail`                                                                                                   | *string*                                                                                                   | :heavy_check_mark:                                                                                         | For blocked, the account's own sentence, safe to show as written. Otherwise a plain phrase about the wait. |
| `clearsItself`                                                                                             | *boolean*                                                                                                  | :heavy_check_mark:                                                                                         | Only while blocked: whether waiting is enough.                                                             |
| `fixUrl`                                                                                                   | *string*                                                                                                   | :heavy_check_mark:                                                                                         | Only while blocked and a person has to act: where to send them.                                            |
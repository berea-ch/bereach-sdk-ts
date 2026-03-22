# SearchConversationsRequest

## Example Usage

```typescript
import { SearchConversationsRequest } from "bereach/models/operations";

let value: SearchConversationsRequest = {
  keywords: "<value>",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `keywords`                                 | *string*                                   | :heavy_check_mark:                         | Search keywords                            |
| `nextCursor`                               | *string*                                   | :heavy_minus_sign:                         | Pagination cursor from a previous response |
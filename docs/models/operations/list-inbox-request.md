# ListInboxRequest

## Example Usage

```typescript
import { ListInboxRequest } from "bereach/models/operations";

let value: ListInboxRequest = {};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `nextCursor`                                           | *string*                                               | :heavy_minus_sign:                                     | Pagination cursor from a previous response             |
| `count`                                                | *number*                                               | :heavy_minus_sign:                                     | Number of conversations to return (default 20, max 40) |
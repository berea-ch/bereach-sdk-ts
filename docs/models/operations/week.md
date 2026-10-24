# Week

## Example Usage

```typescript
import { Week } from "bereach/models/operations";

let value: Week = {
  start: "<value>",
  end: "<value>",
  messages: 128211,
  summary: "<value>",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `start`                                                  | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `end`                                                    | *string*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `messages`                                               | *number*                                                 | :heavy_check_mark:                                       | N/A                                                      |
| `summary`                                                | *string*                                                 | :heavy_check_mark:                                       | Null when this period's summary waits for a later brief. |
# UpsertResults

## Example Usage

```typescript
import { UpsertResults } from "bereach/models/operations";

let value: UpsertResults = {
  created: 565023,
  updated: 767792,
  skipped: 458388,
  errors: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `created`          | *number*           | :heavy_check_mark: | N/A                |
| `updated`          | *number*           | :heavy_check_mark: | N/A                |
| `skipped`          | *number*           | :heavy_check_mark: | N/A                |
| `errors`           | *string*[]         | :heavy_check_mark: | N/A                |
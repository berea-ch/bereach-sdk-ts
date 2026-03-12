# Results

## Example Usage

```typescript
import { Results } from "bereach/models/operations";

let value: Results = {
  created: 986440,
  updated: 722132,
  skipped: 676535,
  errors: [
    "<value 1>",
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
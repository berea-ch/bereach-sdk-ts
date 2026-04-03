# ActiveAccount

## Example Usage

```typescript
import { ActiveAccount } from "bereach/models/operations";

let value: ActiveAccount = {
  id: "<id>",
  name: "<value>",
  plan: "<value>",
  headline: "<value>",
  isUnlimited: true,
  creditsLimit: 402359,
  creditsCount: 310285,
  simulateWrites: false,
  isCurrent: true,
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `id`               | *string*           | :heavy_check_mark: | N/A                |
| `name`             | *string*           | :heavy_check_mark: | N/A                |
| `plan`             | *string*           | :heavy_check_mark: | N/A                |
| `headline`         | *string*           | :heavy_check_mark: | N/A                |
| `isUnlimited`      | *boolean*          | :heavy_check_mark: | N/A                |
| `creditsLimit`     | *number*           | :heavy_check_mark: | N/A                |
| `creditsCount`     | *number*           | :heavy_check_mark: | N/A                |
| `simulateWrites`   | *boolean*          | :heavy_check_mark: | N/A                |
| `isCurrent`        | *boolean*          | :heavy_check_mark: | N/A                |
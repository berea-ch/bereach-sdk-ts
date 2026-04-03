# Subscription

## Example Usage

```typescript
import { Subscription } from "bereach/models/operations";

let value: Subscription = {
  plan: "<value>",
  tier: "<value>",
  proSeatsIncluded: 194218,
  proSeatsUsed: 476341,
  status: "<value>",
  currentPeriodEnd: "<value>",
  hasStripe: true,
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `plan`             | *string*           | :heavy_check_mark: | N/A                |
| `tier`             | *string*           | :heavy_check_mark: | N/A                |
| `proSeatsIncluded` | *number*           | :heavy_check_mark: | N/A                |
| `proSeatsUsed`     | *number*           | :heavy_check_mark: | N/A                |
| `status`           | *string*           | :heavy_check_mark: | N/A                |
| `currentPeriodEnd` | *string*           | :heavy_check_mark: | N/A                |
| `hasStripe`        | *boolean*          | :heavy_check_mark: | N/A                |
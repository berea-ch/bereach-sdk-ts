# GetCampaignStatsWeekly

Current and max weekly usage (null if no weekly cap).

## Example Usage

```typescript
import { GetCampaignStatsWeekly } from "bereach/models/operations";

let value: GetCampaignStatsWeekly = {
  current: 741104,
  limit: 852415,
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `current`          | *number*           | :heavy_check_mark: | N/A                |
| `limit`            | *number*           | :heavy_check_mark: | N/A                |
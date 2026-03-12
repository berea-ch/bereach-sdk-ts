# GetCampaignStatusDaily

Current and max daily usage (null if no daily cap).

## Example Usage

```typescript
import { GetCampaignStatusDaily } from "bereach/models/operations";

let value: GetCampaignStatusDaily = {
  current: 514396,
  limit: 68060,
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `current`          | *number*           | :heavy_check_mark: | N/A                |
| `limit`            | *number*           | :heavy_check_mark: | N/A                |
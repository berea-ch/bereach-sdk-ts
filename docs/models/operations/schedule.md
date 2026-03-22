# Schedule

## Example Usage

```typescript
import { Schedule } from "bereach/models/operations";

let value: Schedule = {
  scheduleId: "<id>",
  type: "<value>",
  state: "Alaska",
  cron: "<value>",
  nextExecution: null,
  lastRunAt: "<value>",
  lastRunStatus: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `scheduleId`       | *string*           | :heavy_check_mark: | N/A                |
| `type`             | *string*           | :heavy_check_mark: | N/A                |
| `state`            | *string*           | :heavy_check_mark: | N/A                |
| `cron`             | *string*           | :heavy_check_mark: | N/A                |
| `nextExecution`    | *string*           | :heavy_check_mark: | N/A                |
| `lastRunAt`        | *string*           | :heavy_check_mark: | N/A                |
| `lastRunStatus`    | *string*           | :heavy_check_mark: | N/A                |
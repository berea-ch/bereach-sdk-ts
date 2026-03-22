# Schedule

## Example Usage

```typescript
import { Schedule } from "bereach/models/operations";

let value: Schedule = {
  scheduleId: "<id>",
  name: "<value>",
  cron: null,
  isPaused: false,
  lastRun: null,
  nextRun: "<value>",
  lastStatus: "<value>",
  destination: "<value>",
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `scheduleId`                                                   | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `name`                                                         | *string*                                                       | :heavy_check_mark:                                             | Human-readable schedule name (e.g. 'DM Polling', 'Draft Send') |
| `cron`                                                         | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `isPaused`                                                     | *boolean*                                                      | :heavy_check_mark:                                             | N/A                                                            |
| `lastRun`                                                      | *string*                                                       | :heavy_check_mark:                                             | ISO 8601 timestamp of last execution                           |
| `nextRun`                                                      | *string*                                                       | :heavy_check_mark:                                             | ISO 8601 timestamp of next scheduled execution                 |
| `lastStatus`                                                   | *any*                                                          | :heavy_check_mark:                                             | Status of the last execution                                   |
| `destination`                                                  | *string*                                                       | :heavy_check_mark:                                             | The endpoint URL this schedule invokes                         |
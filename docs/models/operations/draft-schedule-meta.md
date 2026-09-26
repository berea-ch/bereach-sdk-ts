# DraftScheduleMeta

Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account.

## Example Usage

```typescript
import { DraftScheduleMeta } from "bereach/models/operations";

let value: DraftScheduleMeta = {
  credits: {
    current: 366.87,
    limit: 5982.66,
    remaining: 9003.36,
    percentage: 6374.99,
    isUnlimited: true,
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `credits`                                                                            | [operations.DraftScheduleCredits](../../models/operations/draft-schedule-credits.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |
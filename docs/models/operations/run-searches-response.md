# RunSearchesResponse

The run's receipt

## Example Usage

```typescript
import { RunSearchesResponse } from "bereach/models/operations";

let value: RunSearchesResponse = {
  planId: "<id>",
  state: "done",
  added: 255245,
  alreadyKnown: 870727,
  creditsUsed: 22339,
  costEstimateCredits: 298020,
  searches: [
    {
      id: "<id>",
      label: "<value>",
      state: "searching",
      added: 130190,
      queriesRun: 187312,
      queriesPlanned: 979017,
    },
  ],
  next: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `planId`                                                                         | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `state`                                                                          | [operations.RunSearchesState](../../models/operations/run-searches-state.md)     | :heavy_check_mark:                                                               | N/A                                                                              |
| `stoppedBecause`                                                                 | [operations.StoppedBecause](../../models/operations/stopped-because.md)          | :heavy_minus_sign:                                                               | N/A                                                                              |
| `added`                                                                          | *number*                                                                         | :heavy_check_mark:                                                               | New rows in this list.                                                           |
| `alreadyKnown`                                                                   | *number*                                                                         | :heavy_check_mark:                                                               | People found again: already in this list, or removed from it earlier.            |
| `listTotal`                                                                      | *number*                                                                         | :heavy_minus_sign:                                                               | The list's size after this run, the only running total.                          |
| `leftOut`                                                                        | [operations.LeftOut](../../models/operations/left-out.md)                        | :heavy_minus_sign:                                                               | People left out by the person's own exclusions.                                  |
| `notSaved`                                                                       | [operations.NotSaved](../../models/operations/not-saved.md)                      | :heavy_minus_sign:                                                               | People found but not saved.                                                      |
| `creditsUsed`                                                                    | *number*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
| `creditsLeft`                                                                    | *number*                                                                         | :heavy_minus_sign:                                                               | Absent when the pool is unlimited.                                               |
| `costEstimateCredits`                                                            | *number*                                                                         | :heavy_check_mark:                                                               | The most this run may spend: the plan's ceiling.                                 |
| `searches`                                                                       | [operations.RunSearchesSearch](../../models/operations/run-searches-search.md)[] | :heavy_check_mark:                                                               | N/A                                                                              |
| `notApplied`                                                                     | *string*[]                                                                       | :heavy_minus_sign:                                                               | Plan fields kept for verification later, which nothing checked.                  |
| `notes`                                                                          | *string*[]                                                                       | :heavy_minus_sign:                                                               | The searches' own sentences, to relay as written.                                |
| `runningPlanId`                                                                  | *string*                                                                         | :heavy_minus_sign:                                                               | On busy: the plan whose run is going in this list.                               |
| `next`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | N/A                                                                              |
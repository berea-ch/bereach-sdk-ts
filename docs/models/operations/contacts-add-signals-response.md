# ContactsAddSignalsResponse

Whether a run started, the last run, and the quote

## Example Usage

```typescript
import { ContactsAddSignalsResponse } from "bereach/models/operations";

let value: ContactsAddSignalsResponse = {
  started: false,
  running: false,
  progress: null,
  people: 697187,
  companies: 315619,
  credits: 1347.21,
  run: {
    id: "<id>",
    kind: "email",
    state: "stopped",
    total: 596012,
    done: 195215,
    found: 490310,
    none: 85336,
    failed: 869508,
    skipped: 729810,
    credits: 884.78,
    creditsMax: 6689.9,
    startedAt: "<value>",
  },
  quote: {
    kind: "email",
    people: 60320,
    alreadyDone: 240917,
    credits: 6476.47,
    creditsLeft: 2712.85,
    confirm: true,
    affordable: true,
    affordablePeople: 656994,
  },
};
```

## Fields

| Field                                                                                           | Type                                                                                            | Required                                                                                        | Description                                                                                     |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `started`                                                                                       | *boolean*                                                                                       | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `running`                                                                                       | *boolean*                                                                                       | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `progress`                                                                                      | [operations.Progress](../../models/operations/progress.md)                                      | :heavy_check_mark:                                                                              | The run this call started, else the last run, or null when the list never had one.              |
| `people`                                                                                        | *number*                                                                                        | :heavy_check_mark:                                                                              | People a run reads.                                                                             |
| `companies`                                                                                     | *number*                                                                                        | :heavy_check_mark:                                                                              | Their distinct companies, one news search each.                                                 |
| `credits`                                                                                       | *number*                                                                                        | :heavy_check_mark:                                                                              | The most a run costs, in credits.                                                               |
| `run`                                                                                           | [operations.ContactsAddSignalsRun](../../models/operations/contacts-add-signals-run.md)         | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `quote`                                                                                         | [operations.ContactsAddSignalsQuote](../../models/operations/contacts-add-signals-quote.md)     | :heavy_check_mark:                                                                              | N/A                                                                                             |
| `refused`                                                                                       | [operations.ContactsAddSignalsRefused](../../models/operations/contacts-add-signals-refused.md) | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `stopping`                                                                                      | *boolean*                                                                                       | :heavy_minus_sign:                                                                              | N/A                                                                                             |
| `listUrl`                                                                                       | *string*                                                                                        | :heavy_minus_sign:                                                                              | The list in the app, to give the user.                                                          |
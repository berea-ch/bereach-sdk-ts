# Segment2

## Example Usage

```typescript
import { Segment2 } from "bereach/models/operations";

let value: Segment2 = {
  id: "<id>",
  name: "<value>",
  confidence: "low",
  kinds: [],
  places: [],
  groups: [],
  evidence: [],
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `id`                                                             | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `name`                                                           | *string*                                                         | :heavy_check_mark:                                               | N/A                                                              |
| `confidence`                                                     | [operations.Confidence2](../../models/operations/confidence2.md) | :heavy_check_mark:                                               | N/A                                                              |
| `kinds`                                                          | *string*[]                                                       | :heavy_check_mark:                                               | N/A                                                              |
| `places`                                                         | *string*[]                                                       | :heavy_check_mark:                                               | N/A                                                              |
| `groups`                                                         | [operations.Group2](../../models/operations/group2.md)[]         | :heavy_check_mark:                                               | N/A                                                              |
| `evidence`                                                       | [operations.Evidence2](../../models/operations/evidence2.md)[]   | :heavy_check_mark:                                               | N/A                                                              |
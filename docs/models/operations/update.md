# Update

Fields to update on all matching contacts

## Example Usage

```typescript
import { Update } from "bereach/models/operations";

let value: Update = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `lifecycleStage`                                                                              | [operations.BulkUpdateLifecycleStage](../../models/operations/bulk-update-lifecycle-stage.md) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `hotScore`                                                                                    | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `qualificationNotes`                                                                          | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `notes`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `outreachStatus`                                                                              | [operations.BulkUpdateOutreachStatus](../../models/operations/bulk-update-outreach-status.md) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `nextFollowUpAt`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `doNotContact`                                                                                | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `tags`                                                                                        | *operations.BulkUpdateTagsUnion*                                                              | :heavy_minus_sign:                                                                            | Tag operations: { add, remove } or { set }                                                    |
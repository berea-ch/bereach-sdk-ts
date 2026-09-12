# Update

Fields to update on all matching contacts

## Example Usage

```typescript
import { Update } from "bereach/models/operations";

let value: Update = {};
```

## Fields

| Field                                                                                                   | Type                                                                                                    | Required                                                                                                | Description                                                                                             |
| ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `lifecycleStage`                                                                                        | [operations.DiscardContactsLifecycleStage](../../models/operations/discard-contacts-lifecycle-stage.md) | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `hotScore`                                                                                              | *number*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `qualificationNotes`                                                                                    | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `leadBrief`                                                                                             | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `notes`                                                                                                 | *string*                                                                                                | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `outreachStatus`                                                                                        | [operations.DiscardContactsOutreachStatus](../../models/operations/discard-contacts-outreach-status.md) | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `doNotContact`                                                                                          | *boolean*                                                                                               | :heavy_minus_sign:                                                                                      | N/A                                                                                                     |
| `tags`                                                                                                  | *operations.DiscardContactsTagsUnion*                                                                   | :heavy_minus_sign:                                                                                      | Tag operations: { add, remove } or { set }                                                              |
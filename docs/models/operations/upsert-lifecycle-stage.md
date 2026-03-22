# UpsertLifecycleStage

Lifecycle stage. Defaults to 'contact' on creation. Omit when adding existing contacts to avoid downgrading their stage.

## Example Usage

```typescript
import { UpsertLifecycleStage } from "bereach/models/operations";

let value: UpsertLifecycleStage = "approved";
```

## Values

```typescript
"contact" | "lead" | "qualified" | "approved" | "rejected"
```
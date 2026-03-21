# LifecycleStage

Lifecycle stage. Defaults to 'contact' on creation. Omit when adding existing contacts to avoid downgrading their stage.

## Example Usage

```typescript
import { LifecycleStage } from "bereach/models/operations";

let value: LifecycleStage = "lead";
```

## Values

```typescript
"contact" | "lead" | "qualified" | "approved" | "rejected"
```
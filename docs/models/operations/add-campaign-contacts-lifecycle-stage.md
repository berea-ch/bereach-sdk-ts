# AddCampaignContactsLifecycleStage

Lifecycle stage. Defaults to 'contact' on creation. Omit when adding existing contacts to avoid downgrading their stage.

## Example Usage

```typescript
import { AddCampaignContactsLifecycleStage } from "bereach/models/operations";

let value: AddCampaignContactsLifecycleStage = "rejected";
```

## Values

```typescript
"contact" | "lead" | "qualified" | "approved" | "rejected"
```
# ResultStatus

## Example Usage

```typescript
import { ResultStatus } from "bereach/models/operations";

let value: ResultStatus = "skipped";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"visited" | "cached" | "failed" | "skipped" | "pending" | Unrecognized<string>
```
# Risk

How likely this country/title combination is to return false-positive matches from elsewhere.

## Example Usage

```typescript
import { Risk } from "bereach/models/operations";

let value: Risk = "low";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"low" | "medium" | "high" | Unrecognized<string>
```
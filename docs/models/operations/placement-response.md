# PlacementResponse

Where the people named joined the line, echoed from the request: front (the default) went ahead of everyone already waiting, end went behind the people asked for by name before.

## Example Usage

```typescript
import { PlacementResponse } from "bereach/models/operations";

let value: PlacementResponse = "end";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"front" | "end" | Unrecognized<string>
```
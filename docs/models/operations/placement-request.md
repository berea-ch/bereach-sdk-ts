# PlacementRequest

Where these people join the queue. "front" (default) puts them ahead of everyone already waiting, since naming somebody means this one next. "end" puts them behind everyone named, taking the ordinary place among the rest (most recently active on LinkedIn first, then arrival order); re-calling with "end" for people already in line gives up their front spot. Within one call, the most recently active go first either way.

## Example Usage

```typescript
import { PlacementRequest } from "bereach/models/operations";

let value: PlacementRequest = "end";
```

## Values

```typescript
"front" | "end"
```
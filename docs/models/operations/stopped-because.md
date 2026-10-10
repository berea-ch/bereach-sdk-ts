# StoppedBecause

## Example Usage

```typescript
import { StoppedBecause } from "bereach/models/operations";

let value: StoppedBecause = "market_not_reachable";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"plan_done" | "reached_target" | "out_of_credits" | "daily_limit" | "search_paused" | "market_not_reachable" | "round_limit" | "ceiling_reached" | "search_unavailable" | Unrecognized<string>
```
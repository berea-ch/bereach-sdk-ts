# SearchEmployeesNetworkDistance

LinkedIn network distance: DISTANCE_1=connected, DISTANCE_2=2nd degree, DISTANCE_3=3rd degree, OUT_OF_NETWORK=not connected.

## Example Usage

```typescript
import { SearchEmployeesNetworkDistance } from "bereach/models/operations";

let value: SearchEmployeesNetworkDistance = "OUT_OF_NETWORK";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"DISTANCE_1" | "DISTANCE_2" | "DISTANCE_3" | "OUT_OF_NETWORK" | Unrecognized<string>
```
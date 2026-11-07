# PublicProfileReadFrom

Where a profile read in full was read: the record a search of yours already saved, a public record read today, our index, or the live public page.

## Example Usage

```typescript
import { PublicProfileReadFrom } from "bereach/models/operations";

let value: PublicProfileReadFrom = "records";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"search" | "records" | "index" | "page" | Unrecognized<string>
```
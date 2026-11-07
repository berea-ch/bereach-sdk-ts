# ProfileReadFrom

How fresh the profile is: from a search of yours (search), read today (records, page), or stored earlier (index); readAt says when.

## Example Usage

```typescript
import { ProfileReadFrom } from "bereach/models/operations";

let value: ProfileReadFrom = "search";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"search" | "records" | "index" | "page" | Unrecognized<string>
```
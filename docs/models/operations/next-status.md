# NextStatus

next is first in line, not sent; waiting names the place or the reason; blocked means the account is stopped.

## Example Usage

```typescript
import { NextStatus } from "bereach/models/operations";

let value: NextStatus = "next";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"next" | "waiting" | "blocked" | "not-on-list" | Unrecognized<string>
```
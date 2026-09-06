# Refused

Set when the request could not be searched at all. 'nothing-to-search' means nothing in it named anybody. 'wants-companies' means it asked for organisations, which this operation does not find: use the company search instead. Neither is a retry: say what happened and change the request.

## Example Usage

```typescript
import { Refused } from "bereach/models/operations";

let value: Refused = "nothing-to-search";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"nothing-to-search" | "wants-companies" | Unrecognized<string>
```
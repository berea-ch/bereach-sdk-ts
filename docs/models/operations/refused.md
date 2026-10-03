# Refused

Set when the request could not be answered. 'nothing-to-search' means nothing in it named anybody. 'wants-companies' means it asked for organisations, which this operation does not find: use the company search instead. 'off-topic' means the index answered about a different subject, so nobody it returned was shown: that is a market this search could not reach, never an empty market. None of the three is a retry, say what happened and change the request.

## Example Usage

```typescript
import { Refused } from "bereach/models/operations";

let value: Refused = "nothing-to-search";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"nothing-to-search" | "wants-companies" | "off-topic" | Unrecognized<string>
```
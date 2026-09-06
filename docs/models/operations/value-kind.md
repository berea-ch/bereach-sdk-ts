# ValueKind

How to supply a value: 'enum' = pick a label; 'entity' = pass a name (company/school/etc); 'toggle' = boolean; 'range' = {min,max}; 'text' = free string.

## Example Usage

```typescript
import { ValueKind } from "bereach/models/operations";

let value: ValueKind = "entity";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"enum" | "entity" | "toggle" | "range" | "text" | Unrecognized<string>
```
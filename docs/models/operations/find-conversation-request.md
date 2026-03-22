# FindConversationRequest

## Example Usage

```typescript
import { FindConversationRequest } from "bereach/models/operations";

let value: FindConversationRequest = {
  profile: "<value>",
};
```

## Fields

| Field                                                                                                                                                                           | Type                                                                                                                                                                            | Required                                                                                                                                                                        | Description                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `profile`                                                                                                                                                                       | *string*                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                              | Accepts full profile URLs, vanity names (e.g. marie-sandre), or profile URNs. Direct O(1) conversation lookup via LinkedIn's compose API — no search, no inbox scan. 0 credits. |
| `includeMessages`                                                                                                                                                               | *boolean*                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                              | If true, also return the conversation's recent messages (0 extra credits).                                                                                                      |
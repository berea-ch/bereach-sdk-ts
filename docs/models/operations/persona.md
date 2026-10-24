# Persona

## Example Usage

```typescript
import { Persona } from "bereach/models/operations";

let value: Persona = {
  id: "<id>",
  name: "<value>",
  description:
    "resolve new kissingly strictly reproachfully tragic graceful when harangue",
  criteriaSummary: "<value>",
};
```

## Fields

| Field                                                                                                                                         | Type                                                                                                                                          | Required                                                                                                                                      | Description                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                                          | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `name`                                                                                                                                        | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `description`                                                                                                                                 | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `criteriaSummary`                                                                                                                             | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | Human-readable summary of the persona's filter criteria (e.g. 'VP+ in Sales, US/UK'). Use this to match the user's intent to a saved persona. |
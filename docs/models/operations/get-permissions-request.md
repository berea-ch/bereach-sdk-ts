# GetPermissionsRequest

## Example Usage

```typescript
import { GetPermissionsRequest } from "bereach/models/operations";

let value: GetPermissionsRequest = {
  universalName: "<value>",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `universalName`                                                               | *string*                                                                      | :heavy_check_mark:                                                            | Company URL slug (e.g. 'openai'). Same value as returned by listCompanyPages. |
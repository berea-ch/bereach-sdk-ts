# GetCompanyPagePermissionsRequest

## Example Usage

```typescript
import { GetCompanyPagePermissionsRequest } from "bereach/models/operations";

let value: GetCompanyPagePermissionsRequest = {
  universalName: "<value>",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `universalName`                                                               | *string*                                                                      | :heavy_check_mark:                                                            | Company URL slug (e.g. 'openai'). Same value as returned by listCompanyPages. |
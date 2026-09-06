# CompanyPagePermissionsRequest

## Example Usage

```typescript
import { CompanyPagePermissionsRequest } from "bereach/models/operations";

let value: CompanyPagePermissionsRequest = {
  universalName: "<value>",
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `universalName`                                                               | *string*                                                                      | :heavy_check_mark:                                                            | Company URL slug (e.g. 'openai'). Same value as returned by listCompanyPages. |
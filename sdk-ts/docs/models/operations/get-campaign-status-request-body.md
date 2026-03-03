# GetCampaignStatusRequestBody

## Example Usage

```typescript
import { GetCampaignStatusRequestBody } from "bereach/models/operations";

let value: GetCampaignStatusRequestBody = {
  profiles: [
    "<value 1>",
    "<value 2>",
  ],
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `profiles`                                                              | *string*[]                                                              | :heavy_check_mark:                                                      | LinkedIn profile URLs or URNs to check status for within this campaign. |
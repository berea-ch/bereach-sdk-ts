# CreateCampaignRequest

## Example Usage

```typescript
import { CreateCampaignRequest } from "bereach/models/operations";

let value: CreateCampaignRequest = {
  name: "<value>",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `name`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | Campaign name (e.g., 'lg-engagement-competitor-openai')                          |
| `description`                                                                    | *string*                                                                         | :heavy_minus_sign:                                                               | Optional campaign description                                                    |
| `context`                                                                        | *string*                                                                         | :heavy_minus_sign:                                                               | Full agent instructions in markdown                                              |
| `type`                                                                           | [operations.CreateCampaignType](../../models/operations/create-campaign-type.md) | :heavy_minus_sign:                                                               | Campaign type                                                                    |
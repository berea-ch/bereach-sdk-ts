# PatchSettingsRequest

## Example Usage

```typescript
import { PatchSettingsRequest } from "bereach/models/operations";

let value: PatchSettingsRequest = {};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `country`                                              | *string*                                               | :heavy_minus_sign:                                     | ISO country code                                       |
| `city`                                                 | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |
| `phone`                                                | *string*                                               | :heavy_minus_sign:                                     | N/A                                                    |
| `anthropicKey`                                         | *string*                                               | :heavy_minus_sign:                                     | Anthropic API key (sk-ant-...). Set to null to remove. |
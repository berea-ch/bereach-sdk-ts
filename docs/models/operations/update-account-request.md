# UpdateAccountRequest

## Example Usage

```typescript
import { UpdateAccountRequest } from "bereach/models/operations";

let value: UpdateAccountRequest = {
  accountId: "<id>",
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `accountId`                                                     | *string*                                                        | :heavy_check_mark:                                              | ID of the LinkedIn account to update.                           |
| `label`                                                         | *string*                                                        | :heavy_minus_sign:                                              | User-facing label (e.g. 'Personal', 'Company SDR').             |
| `isDefault`                                                     | *boolean*                                                       | :heavy_minus_sign:                                              | Set as the default account. Clears default from other accounts. |
| `proxyConfig`                                                   | *operations.ProxyConfig*                                        | :heavy_minus_sign:                                              | Proxy config. Null = disable proxy. Object = enable with mode.  |
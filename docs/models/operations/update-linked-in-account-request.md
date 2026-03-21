# UpdateLinkedInAccountRequest

## Example Usage

```typescript
import { UpdateLinkedInAccountRequest } from "bereach/models/operations";

let value: UpdateLinkedInAccountRequest = {
  accountId: "<id>",
};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `accountId`                                                                       | *string*                                                                          | :heavy_check_mark:                                                                | ID of the LinkedIn account to update.                                             |
| `label`                                                                           | *string*                                                                          | :heavy_minus_sign:                                                                | User-facing label (e.g. 'Personal', 'Company SDR').                               |
| `isDefault`                                                                       | *boolean*                                                                         | :heavy_minus_sign:                                                                | Set as the default account. Clears default from other accounts.                   |
| `useProxy`                                                                        | *boolean*                                                                         | :heavy_minus_sign:                                                                | Enable/disable residential proxy for this account.                                |
| `proxyProvider`                                                                   | [operations.ProxyProvider](../../models/operations/proxy-provider.md)             | :heavy_minus_sign:                                                                | Residential proxy provider. Default: decodo.                                      |
| `proxyCountry`                                                                    | *string*                                                                          | :heavy_minus_sign:                                                                | ISO 3166-1 alpha-2 country code for proxy geo-targeting. Null = use user.country. |
| `proxyCity`                                                                       | *string*                                                                          | :heavy_minus_sign:                                                                | City override for proxy geo-targeting.                                            |
| `proxyRotationHours`                                                              | *number*                                                                          | :heavy_minus_sign:                                                                | Sticky IP rotation period in hours (default 24 = 1 day).                          |
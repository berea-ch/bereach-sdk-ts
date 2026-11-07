# FindEmailsRequest

## Example Usage

```typescript
import { FindEmailsRequest } from "bereach/models/operations";

let value: FindEmailsRequest = {};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `contactIds`                                                                                              | *string*[]                                                                                                | :heavy_minus_sign:                                                                                        | Saved people, by the contact ids a contacts or search result returned.                                    |
| `profileUrls`                                                                                             | *string*[]                                                                                                | :heavy_minus_sign:                                                                                        | People by their profile address, saved or not. The email is kept on the contact when the person is saved. |
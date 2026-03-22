# SwitchAccountRequest

## Example Usage

```typescript
import { SwitchAccountRequest } from "bereach/models/operations";

let value: SwitchAccountRequest = {
  credentialsId: "<id>",
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `credentialsId`                                              | *string*                                                     | :heavy_check_mark:                                           | The LinkedIn credentials ID to switch to (from listAccounts) |
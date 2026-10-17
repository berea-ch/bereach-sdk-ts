# DisplayLinkedInConnect

Chat-only connect card marker on the public preview path. autoRetry false means connecting does not start a collect run.

## Example Usage

```typescript
import { DisplayLinkedInConnect } from "bereach/models/operations";

let value: DisplayLinkedInConnect = {
  reason: "<value>",
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `reason`           | *string*           | :heavy_check_mark: | N/A                |
| `autoRetry`        | *boolean*          | :heavy_minus_sign: | N/A                |
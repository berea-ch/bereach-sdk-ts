# MarkSeenRequest

## Example Usage

```typescript
import { MarkSeenRequest } from "bereach/models/operations";

let value: MarkSeenRequest = {
  conversationUrn: "<value>",
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `conversationUrn`                                                                              | *string*                                                                                       | :heavy_check_mark:                                                                             | Full conversation URN (e.g. 'urn:li:msg_conversation:(urn:li:fsd_profile:ACoAAXXX,2-YWUx...)') |
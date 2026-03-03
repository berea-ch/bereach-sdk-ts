# Mention

## Example Usage

```typescript
import { Mention } from "bereach/models/operations";

let value: Mention = {
  profileUrn: "<value>",
  start: 458379,
  length: 790098,
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `profileUrn`                                                                              | *string*                                                                                  | :heavy_check_mark:                                                                        | LinkedIn profile URN of the mentioned person (e.g., 'urn:li:fsd_profile:ACoAABZ0Qo4B...') |
| `start`                                                                                   | *number*                                                                                  | :heavy_check_mark:                                                                        | Start character offset in the text where the mention begins                               |
| `length`                                                                                  | *number*                                                                                  | :heavy_check_mark:                                                                        | Length of the mention text in characters                                                  |
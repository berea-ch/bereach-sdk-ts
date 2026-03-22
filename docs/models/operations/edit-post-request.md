# EditPostRequest

## Example Usage

```typescript
import { EditPostRequest } from "bereach/models/operations";

let value: EditPostRequest = {
  postUrl: "https://fearless-disconnection.name",
  text: "<value>",
};
```

## Fields

| Field                         | Type                          | Required                      | Description                   |
| ----------------------------- | ----------------------------- | ----------------------------- | ----------------------------- |
| `postUrl`                     | *string*                      | :heavy_check_mark:            | LinkedIn post URL or URN      |
| `text`                        | *string*                      | :heavy_check_mark:            | New text content for the post |
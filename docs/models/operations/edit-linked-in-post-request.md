# EditLinkedInPostRequest

## Example Usage

```typescript
import { EditLinkedInPostRequest } from "bereach/models/operations";

let value: EditLinkedInPostRequest = {
  postUrl: "https://weekly-wombat.info/",
  text: "<value>",
};
```

## Fields

| Field                         | Type                          | Required                      | Description                   |
| ----------------------------- | ----------------------------- | ----------------------------- | ----------------------------- |
| `postUrl`                     | *string*                      | :heavy_check_mark:            | LinkedIn post URL or URN      |
| `text`                        | *string*                      | :heavy_check_mark:            | New text content for the post |
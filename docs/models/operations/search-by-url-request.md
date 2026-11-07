# SearchByUrlRequest

## Example Usage

```typescript
import { SearchByUrlRequest } from "bereach/models/operations";

let value: SearchByUrlRequest = {
  url: "https://definitive-comparison.info/",
};
```

## Fields

| Field                                                                                                                                | Type                                                                                                                                 | Required                                                                                                                             | Description                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ |
| `url`                                                                                                                                | *string*                                                                                                                             | :heavy_check_mark:                                                                                                                   | A LinkedIn or Sales Navigator search results link, exactly as the person pasted it. Its keywords, filters and page are read from it. |
| `start`                                                                                                                              | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | Override pagination offset. If not provided, uses the page from the URL (or defaults to 0).                                          |
| `count`                                                                                                                              | *number*                                                                                                                             | :heavy_minus_sign:                                                                                                                   | How many results to return.                                                                                                          |
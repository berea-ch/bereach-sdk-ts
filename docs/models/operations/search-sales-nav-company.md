# SearchSalesNavCompany

Company filter with include/exclude (people only). Use LinkedIn company IDs. Resolve via /search/linkedin/parameters with type='COMPANY'.

## Example Usage

```typescript
import { SearchSalesNavCompany } from "bereach/models/operations";

let value: SearchSalesNavCompany = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `include`          | *string*[]         | :heavy_minus_sign: | IDs to include     |
| `exclude`          | *string*[]         | :heavy_minus_sign: | IDs to exclude     |
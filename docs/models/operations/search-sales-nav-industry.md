# SearchSalesNavIndustry

Industry filter with include/exclude. Use LinkedIn industry IDs. Resolve via /search/linkedin/parameters with type='INDUSTRY'.

## Example Usage

```typescript
import { SearchSalesNavIndustry } from "bereach/models/operations";

let value: SearchSalesNavIndustry = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `include`          | *string*[]         | :heavy_minus_sign: | IDs to include     |
| `exclude`          | *string*[]         | :heavy_minus_sign: | IDs to exclude     |
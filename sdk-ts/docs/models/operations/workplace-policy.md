# WorkplacePolicy

Workplace policy (null when includeWorkplacePolicy is false or data unavailable)

## Example Usage

```typescript
import { WorkplacePolicy } from "bereach/models/operations";

let value: WorkplacePolicy = {
  title: "<value>",
  description: "considering blah alongside best rectangular edge",
  timeAtOnsite: "<value>",
  benefits: [
    "<value 1>",
    "<value 2>",
  ],
};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `title`            | *string*           | :heavy_check_mark: | N/A                |
| `description`      | *string*           | :heavy_check_mark: | N/A                |
| `timeAtOnsite`     | *string*           | :heavy_check_mark: | N/A                |
| `benefits`         | *string*[]         | :heavy_check_mark: | N/A                |
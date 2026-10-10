# PublicFindEmployeesRequest

## Example Usage

```typescript
import { PublicFindEmployeesRequest } from "bereach/models/operations";

let value: PublicFindEmployeesRequest = {
  company: "Kerluke Group",
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `company`                                                                  | *string*                                                                   | :heavy_check_mark:                                                         | The company, by name or by its page address.                               |
| `keywords`                                                                 | *string*                                                                   | :heavy_minus_sign:                                                         | A role to narrow to, written the way people write it on their own profile. |
| `count`                                                                    | *number*                                                                   | :heavy_minus_sign:                                                         | How many people to return.                                                 |
| `more`                                                                     | *boolean*                                                                  | :heavy_minus_sign:                                                         | Continue past the people already returned for this company and role.       |
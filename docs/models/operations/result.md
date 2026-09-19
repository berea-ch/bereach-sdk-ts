# Result

## Example Usage

```typescript
import { Result } from "bereach/models/operations";

let value: Result = {
  input: "<value>",
  profileUrl: "https://squeaky-trolley.biz",
  profileUrn: "<value>",
  publicIdentifier: "<value>",
  status: "<value>",
  error: "<value>",
  cached: false,
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `input`                                                                                               | *string*                                                                                              | :heavy_check_mark:                                                                                    | Echo of what was submitted.                                                                           |
| `profileUrl`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | Canonical /in/<slug> URL when one was found.                                                          |
| `profileUrn`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `publicIdentifier`                                                                                    | *string*                                                                                              | :heavy_check_mark:                                                                                    | The vanity slug, never the encrypted id.                                                              |
| `status`                                                                                              | *string*                                                                                              | :heavy_check_mark:                                                                                    | resolved = a canonical vanity slug; acoa_only = an encrypted id and nothing better; failed = nothing. |
| `error`                                                                                               | *string*                                                                                              | :heavy_check_mark:                                                                                    | A code, present only on failure.                                                                      |
| `cached`                                                                                              | *boolean*                                                                                             | :heavy_check_mark:                                                                                    | True when served from cache, which costs nothing.                                                     |
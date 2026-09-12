# PublicFindJobsResponse

Matched job postings

## Example Usage

```typescript
import { PublicFindJobsResponse } from "bereach/models/operations";

let value: PublicFindJobsResponse = {
  source: "public",
  provider: "<value>",
  query: "<value>",
  jobs: [
    {
      title: "<value>",
      jobUrl: "https://zesty-amendment.com",
      jobId: "<id>",
    },
  ],
  moreAvailable: false,
};
```

## Fields

| Field                                                                                                                                         | Type                                                                                                                                          | Required                                                                                                                                      | Description                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `source`                                                                                                                                      | [operations.PublicFindJobsSource](../../models/operations/public-find-jobs-source.md)                                                         | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `provider`                                                                                                                                    | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The search provider that answered.                                                                                                            |
| `query`                                                                                                                                       | *string*                                                                                                                                      | :heavy_check_mark:                                                                                                                            | The exact query sent, so a thin result set can be read rather than guessed at.                                                                |
| `jobs`                                                                                                                                        | [operations.Job](../../models/operations/job.md)[]                                                                                            | :heavy_check_mark:                                                                                                                            | N/A                                                                                                                                           |
| `moreAvailable`                                                                                                                               | *boolean*                                                                                                                                     | :heavy_check_mark:                                                                                                                            | Whether asking again with more can still reach rows you have not seen. False means this ask is walked out; say so and do not call more again. |
| `duplicates`                                                                                                                                  | *number*                                                                                                                                      | :heavy_minus_sign:                                                                                                                            | Rows a continuation re-reached and dropped as already delivered. Normal bookkeeping, never a failure.                                         |
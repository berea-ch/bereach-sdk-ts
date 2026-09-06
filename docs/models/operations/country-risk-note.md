# CountryRiskNote

A non-blocking caveat about this market, e.g. a country whose profiles are hard to tell apart from a bigger anglophone one. Never a reason to withhold or shrink the result — surface it as a caution alongside the real count, never in place of one.

## Example Usage

```typescript
import { CountryRiskNote } from "bereach/models/operations";

let value: CountryRiskNote = {
  risk: "low",
  reason: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `risk`                                                                                        | [operations.Risk](../../models/operations/risk.md)                                            | :heavy_check_mark:                                                                            | How likely this country/title combination is to return false-positive matches from elsewhere. |
| `reason`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Why, in plain language.                                                                       |
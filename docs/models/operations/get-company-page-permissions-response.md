# GetCompanyPagePermissionsResponse

Company page admin permissions

## Example Usage

```typescript
import { GetCompanyPagePermissionsResponse } from "bereach/models/operations";

let value: GetCompanyPagePermissionsResponse = {
  success: true,
  universalName: "<value>",
  permissions: {
    role: "<value>",
    canCreateOrganicShare: false,
    canCreateComment: true,
    canCreateReaction: true,
    canDeleteShare: true,
    canPinShare: true,
    canSendMessages: false,
    canReadMessages: false,
    canReadAdminDashboard: false,
    canReadOrganizationUpdateAnalytics: false,
    canReadOrganizationVisitorAnalytics: true,
    canReadOrganizationFollowerAnalytics: false,
    canReadOrganizationSearchAppearanceAnalytics: false,
    canUpdateOrganizationProfile: false,
    canEditAdministrators: true,
    canDeactivateOrganization: false,
    canEditEvents: false,
    canReadEvents: true,
    canSponsorShare: true,
    canManageCareerPages: true,
    canManageMessagingAccess: false,
    canNotifyEmployees: false,
    canExportLeads: true,
  },
  creditsUsed: 811397,
  retryAfter: 855335,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `success`                                                                            | *true*                                                                               | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `universalName`                                                                      | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `permissions`                                                                        | [operations.Permissions](../../models/operations/permissions.md)                     | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `creditsUsed`                                                                        | *number*                                                                             | :heavy_check_mark:                                                                   | Credits consumed by this call (0 for free endpoints, cached results, or duplicates). |
| `retryAfter`                                                                         | *number*                                                                             | :heavy_check_mark:                                                                   | Seconds to wait before making another call of the same type. 0 means no wait needed. |
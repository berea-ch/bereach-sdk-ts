# GetPermissionsResponse

Company page admin permissions

## Example Usage

```typescript
import { GetPermissionsResponse } from "bereach/models/operations";

let value: GetPermissionsResponse = {
  success: true,
  universalName: "<value>",
  permissions: {
    role: "<value>",
    canCreateOrganicShare: false,
    canCreateComment: false,
    canCreateReaction: false,
    canDeleteShare: true,
    canPinShare: true,
    canSendMessages: true,
    canReadMessages: false,
    canReadAdminDashboard: false,
    canReadOrganizationUpdateAnalytics: false,
    canReadOrganizationVisitorAnalytics: false,
    canReadOrganizationFollowerAnalytics: true,
    canReadOrganizationSearchAppearanceAnalytics: true,
    canUpdateOrganizationProfile: false,
    canEditAdministrators: true,
    canDeactivateOrganization: true,
    canEditEvents: true,
    canReadEvents: true,
    canSponsorShare: false,
    canManageCareerPages: false,
    canManageMessagingAccess: false,
    canNotifyEmployees: false,
    canExportLeads: true,
  },
  creditsUsed: 709544,
  retryAfter: 796854,
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
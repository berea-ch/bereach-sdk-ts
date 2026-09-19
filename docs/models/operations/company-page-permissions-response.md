# CompanyPagePermissionsResponse

Company page admin permissions

## Example Usage

```typescript
import { CompanyPagePermissionsResponse } from "bereach/models/operations";

let value: CompanyPagePermissionsResponse = {
  success: true,
  universalName: "<value>",
  permissions: {
    role: "<value>",
    canCreateOrganicShare: true,
    canCreateComment: false,
    canCreateReaction: true,
    canDeleteShare: true,
    canPinShare: false,
    canSendMessages: false,
    canReadMessages: true,
    canReadAdminDashboard: true,
    canReadOrganizationUpdateAnalytics: false,
    canReadOrganizationVisitorAnalytics: true,
    canReadOrganizationFollowerAnalytics: true,
    canReadOrganizationSearchAppearanceAnalytics: true,
    canUpdateOrganizationProfile: false,
    canEditAdministrators: false,
    canDeactivateOrganization: true,
    canEditEvents: true,
    canReadEvents: false,
    canSponsorShare: false,
    canManageCareerPages: true,
    canManageMessagingAccess: true,
    canNotifyEmployees: true,
    canExportLeads: true,
  },
  creditsUsed: 234101,
  retryAfter: 300699,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `success`                                                                                                                                 | *true*                                                                                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `universalName`                                                                                                                           | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `permissions`                                                                                                                             | [operations.Permissions](../../models/operations/permissions.md)                                                                          | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `creditsUsed`                                                                                                                             | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Credits consumed by this call. 0 for free endpoints, cached results, duplicates, and for every query that does not touch LinkedIn.        |
| `retryAfter`                                                                                                                              | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Seconds to wait before another call of the same type. 0 means no wait is needed.                                                          |
| `meta`                                                                                                                                    | [operations.CompanyPagePermissionsMeta](../../models/operations/company-page-permissions-meta.md)                                         | :heavy_minus_sign:                                                                                                                        | Credit balance carried on every response so a caller never has to ask for it separately. Absent when the caller has no connected account. |
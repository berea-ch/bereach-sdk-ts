# Permissions

## Example Usage

```typescript
import { Permissions } from "bereach/models/operations";

let value: Permissions = {
  role: "<value>",
  canCreateOrganicShare: false,
  canCreateComment: true,
  canCreateReaction: true,
  canDeleteShare: false,
  canPinShare: false,
  canSendMessages: false,
  canReadMessages: true,
  canReadAdminDashboard: false,
  canReadOrganizationUpdateAnalytics: false,
  canReadOrganizationVisitorAnalytics: false,
  canReadOrganizationFollowerAnalytics: true,
  canReadOrganizationSearchAppearanceAnalytics: true,
  canUpdateOrganizationProfile: false,
  canEditAdministrators: true,
  canDeactivateOrganization: false,
  canEditEvents: false,
  canReadEvents: true,
  canSponsorShare: false,
  canManageCareerPages: true,
  canManageMessagingAccess: true,
  canNotifyEmployees: false,
  canExportLeads: false,
};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `role`                                                                     | *string*                                                                   | :heavy_check_mark:                                                         | Admin role (e.g. 'SUPER_ADMINISTRATOR', 'ADMINISTRATOR', 'CONTENT_ADMIN'). |
| `canCreateOrganicShare`                                                    | *boolean*                                                                  | :heavy_check_mark:                                                         | Can post as the company page.                                              |
| `canCreateComment`                                                         | *boolean*                                                                  | :heavy_check_mark:                                                         | Can comment as the company page.                                           |
| `canCreateReaction`                                                        | *boolean*                                                                  | :heavy_check_mark:                                                         | Can like/react as the company page.                                        |
| `canDeleteShare`                                                           | *boolean*                                                                  | :heavy_check_mark:                                                         | Can delete company page posts.                                             |
| `canPinShare`                                                              | *boolean*                                                                  | :heavy_check_mark:                                                         | Can pin posts on the company page.                                         |
| `canSendMessages`                                                          | *boolean*                                                                  | :heavy_check_mark:                                                         | Can send messages from the company page inbox.                             |
| `canReadMessages`                                                          | *boolean*                                                                  | :heavy_check_mark:                                                         | Can read the company page inbox.                                           |
| `canReadAdminDashboard`                                                    | *boolean*                                                                  | :heavy_check_mark:                                                         | Can access the admin analytics dashboard.                                  |
| `canReadOrganizationUpdateAnalytics`                                       | *boolean*                                                                  | :heavy_check_mark:                                                         | Can view post/update analytics.                                            |
| `canReadOrganizationVisitorAnalytics`                                      | *boolean*                                                                  | :heavy_check_mark:                                                         | Can view visitor analytics.                                                |
| `canReadOrganizationFollowerAnalytics`                                     | *boolean*                                                                  | :heavy_check_mark:                                                         | Can view follower analytics.                                               |
| `canReadOrganizationSearchAppearanceAnalytics`                             | *boolean*                                                                  | :heavy_check_mark:                                                         | Can view search appearance analytics.                                      |
| `canUpdateOrganizationProfile`                                             | *boolean*                                                                  | :heavy_check_mark:                                                         | Can edit the company page profile.                                         |
| `canEditAdministrators`                                                    | *boolean*                                                                  | :heavy_check_mark:                                                         | Can add/remove page admins.                                                |
| `canDeactivateOrganization`                                                | *boolean*                                                                  | :heavy_check_mark:                                                         | Can deactivate the company page.                                           |
| `canEditEvents`                                                            | *boolean*                                                                  | :heavy_check_mark:                                                         | Can create/edit company events.                                            |
| `canReadEvents`                                                            | *boolean*                                                                  | :heavy_check_mark:                                                         | Can view company events.                                                   |
| `canSponsorShare`                                                          | *boolean*                                                                  | :heavy_check_mark:                                                         | Can sponsor/boost posts.                                                   |
| `canManageCareerPages`                                                     | *boolean*                                                                  | :heavy_check_mark:                                                         | Can manage the career page section.                                        |
| `canManageMessagingAccess`                                                 | *boolean*                                                                  | :heavy_check_mark:                                                         | Can manage messaging settings.                                             |
| `canNotifyEmployees`                                                       | *boolean*                                                                  | :heavy_check_mark:                                                         | Can notify employees about posts.                                          |
| `canExportLeads`                                                           | *boolean*                                                                  | :heavy_check_mark:                                                         | Can export lead-gen form leads.                                            |
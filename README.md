# aws-scp-policies

## Purpose

- Service control policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization.
- SCPs offer central control over the maximum available permissions for all accounts in your organization.
- SCPs help you to ensure your accounts stay within your organization’s access control guidelines.
- SCPs are available only in an organization that has all features enabled.
- SCPs alone are not sufficient to granting permissions to the accounts in your organization.
- No permissions are granted by an SCP.
- An SCP defines a guardrail, or sets limits, on the actions that the account's administrator can delegate to the IAM users and roles in the affected accounts.
- The administrator must still attach identity-based or resource-based policies to IAM users or roles, or to the resources in your accounts to actually grant permissions.
- The effective permissions are the logical intersection between what is allowed by the SCP and what is allowed by the IAM and resource-based policies.

## SCP Best Practices

- Use Deny statements whenever possible
- Only six SCPs can be attached to each account, so combination SCPs are best
- SCPs are limited to 512kb, which means you should elimintae white space wherever possible and use deny statements, as they are smaller in size
- SCPs should ONLY be used IF they will effect ALL accounts within an organization
- IAM policies should be used for anything effecting a single account


## Troubleshooting SCP policies

- If using any of the SCPs listed here, and the following need to be worked on, you will need to coordinate with an account holder in the Organizational account
  - Password change policy
  - Cloudtrail delete
  - Changing FOR users' access
  - Changing access to the organization
  - Changing access to the Account portal
  - Changing access to Billing
  - Changing Root-User Access
  - Etc.

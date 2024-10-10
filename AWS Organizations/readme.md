### AWS Organizations

- **Purpose**: Manage multiple AWS accounts, enhance security, and streamline billing.

### Service Control Policies (SCPs)
- **Purpose**: Manage permissions across accounts by **restricting** access.
- **Key Points**:
  - SCPs do **not grant permissions**, only restrict them.
  - SCPs override IAM or resource-based policies.
  - **Do not apply** to management account and root user.
  - Apply to all accounts under an Organizational Unit (OU), e.g., applying SCP to "Finance OU" enforces it across all users/accounts in that OU.
  - SCPs **do not apply** to service-linked roles, resource-based policies, or external accounts.

### Management Account
- **Central Authority** for creating and managing policies, billing, and overall governance in the organization.

### Additional Notes
- By default, newly created AWS accounts have a role called **"OrganizationAccountAccessRole"** (grants full admin rights). 
- Use **SCP** to limit or deny access to this role if necessary.
- For existing accounts, this role needs to be added manually.
- To access multiple accounts within an organization, use **IAM Identity Center** or **Switch Role**.

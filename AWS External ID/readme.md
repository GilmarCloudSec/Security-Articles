### External ID
- **Purpose**: A security mechanism to protect against the "confused deputy" problem in cross-account role access.
- **Usage**: Typically used when granting third-party access to your AWS resources.
- **Confused Deputy Problem**: This occurs when a third-party service, which has permissions to assume roles, is tricked into accessing resources it shouldn't.

### Example Scenario
- When a third-party service (like a monitoring tool or backup service) needs access to your AWS resources (e.g., S3 bucket):
  - Create a role granting specific access.
  - **External ID** is shared with the third party.
  - The third party must use the **External ID** when assuming the role, ensuring only the intended party can access the resources.

### Example Trust Policy (with External ID)
- **Trust Policy**: Defines permissions for cross-account access, ensuring only the third-party with the correct External ID can assume the role.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "AWS": "arn:aws:iam::ACCOUNT_NUMBER:root"
      },
      "Action": "sts:AssumeRole",
      "Condition": {
        "StringEquals": {
          "sts:ExternalId": "EXTERNAL_ID_VALUE"
        }
      }
    }
  ]
}
```

### Key Points to Remember:
1. **External ID** is used to prevent unauthorized third parties from assuming roles in your account.
2. It adds an extra layer of protection by requiring the third-party to provide the correct External ID.
3. **Condition in Trust Policy**: The role assumption is allowed only when the correct External ID matches (via the `sts:ExternalId` condition).


### AWS IAM Roles

- **Purpose**: 
  - Grants permissions by providing **temporary credentials** (not stored in the application).
  - Credentials are **automatically rotated** and **expire** after a defined duration.

- **Usage Scenarios**:
  - **EC2 Instances**: Attach an IAM role directly to the instance to provide the required permissions.
  - **External Users**: Create a role with a **trust policy** that allows users to assume the role and attach necessary permissions.

- **Benefits**:
  - Facilitates **least privilege** for specific tasks.
  - Offers a **clear audit trail** for tracking actions (e.g., tracking the use of the "SecurityAnalyst" role).
  - Supports **cross-account access**.

- **Revoking Temporary Credentials**:
  - To revoke access, navigate to the role and click **"Revoke Active Sessions"**, which will generate an inline policy to address the issue.

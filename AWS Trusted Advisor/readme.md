### **AWS Trusted Advisor**

**Overview:**
- AWS Trusted Advisor provides health checks and best practice recommendations by comparing your current AWS setup against established best practices.

#### **Security Tab Checks:**

1. **Basic Plan Checks:**
   - **MFA on Root Account**: Ensure Multi-Factor Authentication is enabled for enhanced security.
   - **EBS Public Snapshots**: Check for any Elastic Block Store (EBS) snapshots that are publicly accessible.
   - **RDS Public Snapshots**: Review Amazon RDS snapshots for public accessibility.
   - **Security Groups**: Identify security groups that allow inbound traffic from 0.0.0.0 (open to all).
   - **S3 Bucket Permissions**: Monitor S3 bucket settings to prevent open access.

2. **Premium Plan Checks:**
   - Offers a broader range of security checks.

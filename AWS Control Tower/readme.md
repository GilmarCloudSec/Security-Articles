### **AWS Control Tower**
- **Purpose:** Simplifies setting up and managing a secure multi-account AWS environment by integrating services like **AWS Organizations**, **AWS Config**, and **AWS CloudTrail**.
- **Key Feature:** Use of **Account Factory** to automate the creation of new AWS accounts with security best practices.

### **Key Components:**
1. **Log Archive Account**:  
   - Central repository for logs from all AWS accounts.
   - Collects **CloudTrail logs**, **Config logs**, **VPC Flow Logs**, etc.
  
2. **Audit Account**:  
   - Used for active security monitoring, compliance, and security analysis.
   - Uses services like **Security Hub**, **GuardDuty**, and **CloudWatch** to access and analyze logs from the Log Archive account.

### **Deployment Considerations:**
- **Service Restrictions for Successful Deployment:**
  - **AWS Organizations**: Don't manually add accounts; use **Control Tower's Account Factory** instead.
  - **Guardrails**: Prefer using **Control Tower Guardrails** over directly managing Service Control Policies (SCPs).
  - **CloudTrail**: Adjust or deactivate existing CloudTrail configurations to prevent duplicate logging.
  - **AWS Config**: Modify or remove conflicting AWS Config configurations that may cause deployment issues.

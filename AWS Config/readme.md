### **AWS Config Overview:**
- **Purpose:** Records and tracks configuration changes across AWS resources, allowing visibility into resource history.
- **Primary Functions:**
  - **Identify Unauthorized/Accidental Changes:** Monitor changes to detect potential security issues.
  - **Track Compliance:** Ensures resources adhere to regulatory standards.
  - **Troubleshoot Issues:** Use change history to identify the root cause of problems.
  - **Analyze Resource Usage:** Gain insights into resource usage and optimization opportunities.

### **Key Points:**
- **Configuration Tracking:**
  - **Records Changes in S3:** Configuration changes are recorded in an S3 bucket when enabled.
  - **Cannot Prevent Changes:** AWS Config only tracks changes but does not stop them from happening.
  
- **Rules:**
  - **AWS Managed & Custom Rules:** You can either use pre-defined AWS rules or create custom ones to enforce specific compliance checks.
  - **Notifications:** Use SNS to set up alerts when specific rule conditions are met.
  - **EventBridge Integration:** Config sends events to EventBridge on compliance status changes, triggering automated remediation (e.g., Lambda functions).
  
- **Remediation:**
  - **Lambda Automation:** Lambda can be triggered for auto-remediation based on changes detected.
  - **Systems Manager:** Only handles remediation for EC2 instances.

### **Advanced Config Features:**
- **Conformance Packs:**
  - A set of rules and remediation actions bundled together. Templates can be created via CloudFormation or AWS-managed templates.
  - **Example:** Security Best Practices for Lambda template.

- **Aggregators:**
  - **Cross-Region Support:** While Config is regional, Aggregators allow you to track resource changes across multiple regions.

### **Service-Linked Role (SLR)**

- **Purpose**: Allows AWS services to act on your behalf and interact with other AWS resources. AWS manages predefined **permissions** and **trust policies**.
  
- **Key Difference**:
  - **SLR**: AWS automatically creates and manages the trust and permissions policies.
  - **Regular IAM Role**: You (the user) define both the trust and permissions policies.

- **Use Case**: For services like **CloudTrail**, which needs to access various AWS services (e.g., S3 for storing logs, CloudWatch for monitoring).

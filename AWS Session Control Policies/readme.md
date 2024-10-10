### **Session Control Policies Overview**
- **Purpose**: Restrict permissions for **role sessions** and **federated sessions** via CLI or API calls.
- **When to Use**: To **temporarily limit permissions** granted to a user or role for a specific task or context.

#### **Role Assumption**:
- **What It Does**: When assuming a role, you can attach a **session policy** to limit the actions that can be performed.
- **Example**: If a role has broad permissions, a session policy can restrict actions for the session without altering the role’s default permissions.

#### **Federated Users**:
- **Usage**: Session policies can also limit what a **federated user** can do, even if their federated identity grants broader permissions.


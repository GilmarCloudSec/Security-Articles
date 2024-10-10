### **IAM Identity-Based Policies**
- **Inline Policies**:
  - **Granular Control**: Directly attached to a single IAM identity (user, group, or role).
  - Suitable for small environments but become difficult to manage as user count grows.
  - Example use: Denying or allowing actions for specific users.
  - When attached to a user, **no need to specify the Principal**, as it's implicitly associated.

- **Managed Policies**:
  - **Flexible and Scalable**: Ideal for large environments where policies need to be reused.
  - **Centralized**: Can be attached to multiple users, groups, or roles simultaneously.
  - Simplifies policy management as your environment grows.

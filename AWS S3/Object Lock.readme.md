### **S3 Object Lock:**
- **Purpose**: Prevents objects from being deleted or overwritten for a fixed period or indefinitely.
- **Requirements**: 
  - **Versioning** must be enabled.

### **Retention Management:**
1. **Retention Periods**:
   - **Lock individual objects or entire S3 bucket** for a specified time (e.g., 24 hours).
  
2. **Retention Modes**:
   - **Compliance Mode**:
     - No user, including root, can delete or overwrite objects during the retention period.
   - **Governance Mode**:
     - Prevents most users from deleting or overwriting objects, but allows permissions for some users (e.g., admins) to make changes.

3. **Legal Hold**:
   - Has **no expiration date**.
   - Must be removed explicitly using the `s3:PutObjectLegalHold` IAM permission.


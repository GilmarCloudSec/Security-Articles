### Key Points on Resource-Based Policies:

**Definition**: Resource-based policies are directly attached to resources (such as S3 buckets, roles, etc.), specifying which identities (users, roles, or accounts) can access them and what actions they can perform.

**Principal Element**: In resource-based policies, you must define the **Principal**, which identifies who (person, service, or account) is allowed access to the resource.

 **Example 1 – User Access**:
   - The policy grants specific access (e.g., "s3:ListBucket") to a specific user (e.g., Alice) for an S3 bucket.
   ```json
   {
     "Effect": "Allow",
     "Principal": { "AWS": "arn:aws:iam::1764463632:user/Alice" },
     "Action": "s3:ListBucket",
     "Resource": "arn:aws:s3:::my-bucket"
   }
   ```

 **Example 2 – Role Assumption by EC2**:
   - The policy allows EC2 to assume a specific role (e.g., MyEC2Role) to perform actions like obtaining temporary security credentials.
   ```json
   {
     "Effect": "Allow",
     "Principal": { "Service": "ec2.amazonaws.com" },
     "Action": "sts:AssumeRole",
     "Resource": "arn:aws:iam::5474567567:role/MyEC2Role"
   }
   ```

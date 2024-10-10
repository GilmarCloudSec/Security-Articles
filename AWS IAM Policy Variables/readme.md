### IAM Policy Variables Overview

- **Purpose**: IAM policy variables are used to customize access control within AWS IAM policies based on specific attributes, enhancing security and manageability.

- **Use Case**: Ideal for scenarios where users need access to personal resources within a shared structure, such as a "Finance Department" containing subfolders for individual users.

### Example Scenario

- **Folder Structure**: Each user in the Finance Department has a personal folder under a main directory (e.g., "finance department").

- **Policy Example**:
  - Allows users to perform specific actions (e.g., `s3:GetObject`, `s3:PutObject`) only on their respective subfolders.
  - The policy utilizes the `{aws:username}` variable to restrict access.

### Example: IAM Policy Variable 

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:GetObject",
                "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::finance department/${aws:username}/*"
            ]
        }
    ]
}
```


### Benefits of Using IAM Policy Variables

- **Streamlined Access Management**: Simplifies the process of granting permissions to users based on their identities, minimizing administrative overhead.
  
- **Enhanced Security**: Ensures that users can only access their data, reducing the risk of unauthorized access to others' folders.

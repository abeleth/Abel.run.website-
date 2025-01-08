+++
title = 'AWS.'
date = 2024-08-17T18:13:50-06:00
draft = false
+++



Sign in to the AWS Management Console
Log in to the AWS Management Console and navigate to the IAM service from the "Security, Identity, & Compliance" section.



<img src="themes/hugo-profile-new/images/Screenshot 2025-01-07 234543.png"  width="600" height="200" />










Navigate to the "Users" Section
In the IAM dashboard, click on Users in the left-hand menu.
Click the Add users button to initiate the user creation process.

Configure User Details
Specify the User Name: Enter a unique name for the user (e.g., "devops-user" or "team-member-1").
Select Access Type:
Programmatic access: Assign this if the user needs an access key ID and secret access key to use AWS CLI, SDKs, or APIs.
AWS Management Console access: Assign this if the user will log in to the console. You can also enable a custom password.

Set Permissions
Choose one of the following methods to assign permissions:
Add user to group: Assign the user to an existing group with pre-defined policies (e.g., AdministratorAccess, ReadOnlyAccess).
Attach policies directly: Manually select policies to apply directly to the user.
Copy permissions from an existing user: Duplicate permissions from an existing user for consistency.

Review Tags (Optional)
You can add metadata in the form of key-value pairs (tags) for easier identification and management of resources (e.g., Role: DevOps or Team: Engineering).

Review and Create User
Verify all settings on the Review page.
Click Create user to

[def]: <Screenshot 2025-01-07 234543.png>
[def2]: <../../themes/hugo-profile-new/images/Screenshot 2025-01-07 234543.png>
[def3]: <../../themes/hugo-profile-new/images/Screenshot 2025-01-07 234543.png>
[def4]: <../../themes/hugo-profile-new/images/Screenshot 2025-01-07 234543.png>
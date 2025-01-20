<details>
  <summary>How to create a user in AWS?</summary>

### Solution


Go to the AWS IAM service

Click on "Users" in the right side menu (right under "Access Management")

Click on the button "Add users"

Insert the user name (e.g. mario)

Select the credential type: "Password"

Set console password to custom and click on "Next"

Click on "Add user to group"

Insert "admin" as group name

Check the "AdministratorAccess" policy and click on "Create group"

Click on "Next: Tags"

Add a tag with the key Role and the value DevOps

Click on "Review" and then create on "Create user"

### How to use Terraform to creat IAM AWS user.

```

 
resource "aws_iam_group_membership" "team" {
  name = "tf-testing-group-membership"

  users = [
    aws_iam_user.newuser.name,

  ]

  group = aws_iam_group.admin.name
}

resource "aws_iam_group_policy_attachment" "test-attach" {
  group      = aws_iam_group.admin.name
  policy_arn = "arn:aws:iam::aws:policy/AdministratorAccess"
}
resource "aws_iam_group" "admin" {
  name = "admin"
}

resource "aws_iam_user" "newuser" {
  name = "newuser"
  path = "/system/"

  tags = {
    Role = "DevOps"
  }
}
'''
</details>

<details>
  <summary>How to create a password Policy in AWS?</summary>

### Password Policy:

Go to IAM service in AWS
Click on "Account settings" under "Access management"
Click on "Change password policy"
Check "Enforce minimum password length" and set it to 8 characters
Check "Require at least one number"
Check "Prevent password reuse"
Click on "Save changes"

MFA:

Click on the account name

Click on "My Security Credentials"

Expand "Multi-factor authentication (MFA)" and click on "Activate MFA"

Choose one of the devices

Follow the instructions to set it up and click on "Assign MFA"

### How to do it on Terraform

'''
resource "aws_iam_account_password_policy" "strict" {
  minimum_password_length        = 8
  require_numbers                = true
  allow_users_to_change_password = true
  password_reuse_prevention      = 1
}
'''

</details>

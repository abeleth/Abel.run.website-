<details>
  <summary>How to create a user?</summary>

Solution
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

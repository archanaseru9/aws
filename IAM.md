# AWS Securities:
- cloud security is highest priority
- compared to on-premises environment, AWS security provides a high level of data protection at low cost to its user
  # Types of securities:
  - IAM: Identity access management .create groups allow user to access service or deny them..no charge for this service
  - KMS
  - cognito :
  - WAF
# IAM workflow includes following resources:
- Principal: Action on AWS resource can be performed by principal . User or role can be pricipal 
- Authentication: Authentication is a process of confirming the identity of the principal trying to access an AWS product. To authenticate from console ,API or CLI , you must provide your credentials or required keys
- Request : When principal attemps to access the AWS console,PAI or CLI ,he sends request to AWS
- Authorozation : IAM user information from request context to check for matching policies and determine whether  to allow  or deny request
- Actions: After authentication and authorizing request , aws approves action. using action , you can review ,create,edit and delete resources
- Resources : set of actions performed on  in a related resource of your AWs account.

  # COmponent of IAM:
  - user: with IASm, securely manage access to AWS services, you can create IAM user where there is new employee to your corporate. ecah IAM user associated with only one AWS account
  - policies : sets permission and controls the access to IAM resources, policies stores in AWS as JSON documents, permission specify  who can have access to resource  and what actions they can perform 
  - roles: temporary credentials.
  - Group: collection of  IAM users is an IAM group. you can use IAM group to specify permisson for multiple users,so that any permission applied to the group , are applied to its users as well.
  -  set permission to group atomatically apply to the users in the group
 # types of policies:
- Managed policies: it is default policy that attch to multiple entities (user,group,roles) in you AWS account
-   - AWS managed policies;
    -  coustom managed policy
- Inline polices:  you can create your own policy that is embedded directly into a single entity (user,group,role)
- 
# role:
- set of premissions that define what actions allowed and denied by entity in AWS console
- it is similar to user
-  a role in IAM can be accessed by any entity (individual or AWS service)
  # create a role with policies to access S3 bucket from EC2 instance and attach role to EC2 instance

  # Features of IAM:
  - share access to  your IAM account
  - Granular permissions
  -  Secure access to AWS resources  for applications running on EC2
  -  Mutifactor authentication (MFA)
  -  identity federation
  -  free to use
  -  PCI DSS compliance
  -  password policy 

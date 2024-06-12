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
- Resources

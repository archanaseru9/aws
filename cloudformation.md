# cloud formation:
- managing instrasture with multiple service is tedious task, rebuilding  your infrastracture and application when necessary can be challenging anf time consuming
- AWS CLOUD FORMATION provides users with a simple way to create and manage a collection of AWS resources by provisioning and updating them in an orderly and predictable way
- collection of AWS resource is called stack
- AWS cloud formation enables you to manage your complete infrastructure through text file

- all resources required by application can be deployed easily by using templates
- reuse your template to replicate your infrastructure in multiple environments
- To make template reusable , use the parameters,mapping conditions selections in the template so that you can customize your stacks when you create them
-  create or use existing cloud formation template using JSON/YAML format.
-  save your code template locally or in s3 bucket
-  use AWS cloudformation to create stack on your template
-  cloud formation constructs the stack in AWS
# AWS cloudformation concepts
# 1.template : is formates in text or json , that describe AWS infrastructure
  - templates in cloudformation consists of nine mine objects:
      1. format version: format version defines the capability of template 
      2. Description: any comment 
      3. meta data: can be used in the template to provide furthur information using JSON or YAML object
      4. parameters: templates can be customized using parameter
          - each time you create or update your stack,parameters help in giving custom values to your template at runtime
      5. mappings : mapping enables you to map keys to acorresponding named values that specify in conditional parameter
         - you can also retrive values in may by using Fn:FindInMap intrinsic function
      6. conditions: can be used when you want to reuse the template by creating resource in different context
          - in template, during stack creation,all conditions in tyour template are evaluated
          - any resources that are associated with a true conditions are created and invalid conditions are ignored automatically
          -  ex: FN:: EQUALS, FN::IF , FN::OR ,FN::AND
      7. Transform: builds a declatrative language for AWS cloudformation and enables reuse of template components
      8.resources: Using resource section,declare the AWS resource that you want to create and specify in the stack , such as Amazon S3 bucket or AWS lambda
      10. outputs : output that values that you can import into other stacks or the values that are returned when a user view his own stack properties
    ## template resource attributes:
        #- creation policy: associate the creation policy attribute with a resource when you want to delay or resource configuration action before proceeding with stack creation
      - with this attribute stack creation is delayed , untill AWS cloudformation receives a specified number of success signals
      - it can be used only for AWS autoscaling , AWS EC2 instance and AWS cloudformation

# -deletion policy:
  - using deletion policy , preserving and backing up of resource is possible when stack is deleted.
  - by default, AWS cloudformation deletes the resource and all its content if a resource has no deletion policy attribute in template
  - before deleting a resource, AWS cloudformation creates its snapshot
  -  " Retain Deletion policy" , if the resource have the deletion policy have the "Retain", when the stack is deleted, AWS cloud formation leaves the bucket without deleting
# Depends on: 
 - depends on attribute in a template, any user can define  the creation of specific resource followed by another resource
# update policy: 
  - with this attribute in AWS cloud formation,you can manage and replace the updates of the instances in auto scaling group 
# 2.stack
 - collection of AWS resource is called a stack and it can be manages in single unit
 - cloud formation's templates define a stack in which the resource can be created ,deleted or updated in predictable way
 - stack can have all resources that can be required to run a web application 
   # Nested stacks:
      - nested stacks  result a hirarchy of stacks
      - using the cloud formation stack resource, a user can create nested stack with in another stack
   # windows stack:
      - windows stack gives you the ability to update and configure your own stack in windows instance
      - with AWS cloud formation, you can create microsoft windows stack for amazon EC2 windows AMI
  ## StackSet:
  - using AWS cloudforamtion template, you can define  a stackset that lets you to create stack in AWS account the globe by using single template
  - after stack set defined by you , updating or deleting the stack in target account  and regions are also can be  specified
# cloudformation access control:
  - IAM user: with IAM, cloud formation can have access control for user and ensure the only IAM user can create,update and delete stacks
  - service role: on the users behalf, service role allow AWS cloudformation to make calls to resource in a stack
  - stack policy: it is applied to all AWS  cloudformation users who attempt to update the stack. Here, you cannot include different users with differeent stack policies


https://www.youtube.com/watch?v=uQdzcIf_KII&t=17519s

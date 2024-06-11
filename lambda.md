# Lambda :
-  dont requires server , all need ti write the code and upload it to  lambda. automatically scalling is done based on size of workload. it scales the application running the code in response to each trigger
-  metering the seconds, bill  only for the amount of time code is running . i.e your not charged of running any server
-  lamda is one of compute service which AMW provides
-   Compute services:
-    - Amazon EC2
     - amazon EBS
     -  amazaon elastic load balancing
     -  AWS lambda
- lamda trriger the services based on the application  mentioned in code. supported  no.of prominent programming languages like node.js,java,c#, python etc
- bases on event run function
  # use cases:
- process imgaes whhen it is uploaded to s3 backet.
-   addning images to s3 bucket and aws lambda is triggered , the images are processed and converted into thumbnails based on the device
  # anamyse social media data
   - hash tag..  when their is data with # has tag, lambda triggers and store the data in data base
     - some companied,coca cola ,benchling etc
  # how lambda works :
  - which client triggers the lambda, lambda with single request create the container . so the request given to container to handle . A container contains the code the user has to provided to satisfy the query
 - use case:
 -  there are 2 bucket .. one is store data and one is to back up the data
 -   create a IAM role  and policies fir the bucket access
  - create labda function to copy the stored bucket to backe up data. this lambda function triggers when there is any change in metadata of stored bucket  and then testing it out
    
       

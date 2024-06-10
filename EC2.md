##EC2:
# choosing AMI
- AMI  or amazon machine image is template used to create machine or new instance based on requirement
- AMI contains software information, access permission, operating system information ,volume information
-  ALIs are 2 types: predefined AMIs and custome AMIs
- Predefined AMI created by AMzaon and modulfied by users
- Custom AMIs created bu users that can be reused
# Instance Type:
-  it specifies hardware  specification required  in the machine choosing from above step.
-  divided into 5 stpes:
-  compute optimized : lot of processing 
-  storage optimized: storage service
-  GPU optimized: large graphical  gaming purpose, graphical requirements
-  memory optimized: if application requires in memory cache for readind and processing
-  general purpose : general purpose, not specific about family..balanced all components
- # configure instacne:
-  purchasing options: on demand, use and pay, on spot
-  network information : what kind of network and subnet , when to assign public ip and ,
-  IAM role
-   shutdown behaviour : shut down or terminate
  # advanced :
  - boot strap the instance with scripts: run commands beofre handover to instance,
  - payment option: normal payment, reserve instance, spot instacne
    # add storage:
    - ephermiral storage( temoprary and free)
    -  amazon elastic block store ( permanent and paid )
    - amazon s3
    - this sizes are in (GBs), volume type , the location where the disk is mounted and where volume needs to be encrypted
    - Free users get to access up to 30GBs of SSD or magnetic storage
    - # tags:
    - - to filter the instance 
    - # security Groups:
    - - - protect the EC2 instance by specifiying inbound and outbound traffic and firewall rules, port number and access method
      - # review and lunch instance
     
      - - select choose key pair  or create new key pair.

         putty gen  used to convert pem to ppk
        -- ppk file used to login ec2 instace using putty


        ### SNS : help us to giving notification to customers
        - got to SNS and create topic
        - make sure the topic is public
        - add subscribers
        - create s3 bucket
        - create event to trigger notification to service
        -  so, notification is sent to your subscribers every time you add something to your bucket ,through email
        -  - sysnc S3 bucket to  AWS instace

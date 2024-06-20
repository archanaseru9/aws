# virtual private cloud:
## Amazon VPC ans subnets:
# AMAzon VPC terminology:
 - VPC (virtual private cloud): VPS enables you to launch AWS resources  into virtual network that you defined .VN  resembles the traditional network  thay operate in own data center, that benifits of using  sclable infrastructre of AWS
 - #-elastic IP adress:to make public IP addresss to retain if it the instace got deleted elastic IP is used.  IP adreess with be permenantly assosicated with account and it will be chargeble.elastic IP adress to be used to associate with NAT gateway
 - #-subnets: Range of IP address in your VPC.you can lunch the AWS resource into subnet that you select. use public subnet for resource  that must be connected to the internet and private subnet for the resources that won't connect to the internet
 - #-Route table:
 -   -  route table contains set of rules called routes, which are used to determine where network traffic is directed
     -  each subnet in VPC must associated with route table.table controls the routing for the subnet. subnet can only be  associated with one route table at a time.but you can associate multiple subnets with same route table.
 - 
 -  #- Internet gateway: internet gateway is horizontally scaled,redundant,and highly  available component that allows communication between instacne in your VPS and internet. it therefore imposes no availabilty risks or bandwidth constrains on your network traffic
 -   - to get internet access:
     -  1. internet gateway must attached to the VPC
        2. all instance in the subnet must have public IP or elastic IP
        3. subnet route table point to the internet gateway
        4. all network access control and security group rules must be configured to allow the required traffic to and from your instance
 - #- VPC NAT devices
 -  --- use can use NAT device to get the private subnet to the internet access.. line database still need to connect to AWS resource in internet
 -  there are 2 differeent NAT devices NAT gateway and NAT instance(NAT instance in AMI)
 - #- NAT gateway: need to be created in public subnet with elastic IP to get access to the internet, and cretae routable and can access resource in  the private subnet 
 - #- NETwork ACLS:
 -  - network access control list(ACL) is an optional layer of security of your VPC that acts as firewaall for controlling traffic in and out of one or more subnets
    -  you might set up network ACL with rules similar  to your security group in order to add an additional  layer of security to your VPC
    -  network ACL setup between subnet and route table
    -   each subnet in VPC must be associate with ACL
    -   subnet can be associates with one ACL, but ACL can be associated with multiple subnets
    -   ACL contains a list of numbered rules with are evaluated in order starting with lowest
    -   ACL ae stateless, responses to allowed inbound traffic are subjected to the rules for outbound traffic
 - # security groups : security group acts as virtual firewall that controls the traffic for one or more instances. you add rules to each security group that allow tarffic to or from its associated instances
 -   - webserver security group:
     -  http TCP 80
     -  https TCP 443
     -  ## 1. by default security group allows all outbound traffic
     -  2. security group rules are always permmisive
        3. security groups are state ful
        4. you can modify the rules of security group at any time and rules are applied immediately
 - # VPC limitations:
 -  5 VPCs per region
 -  200 subnets per VPC
 -  200 routetables per VPC
 -   550 secuirity groups per VPC
 -   50 inbound or outbound rules per VPC
 -   some rules can be raised by raising ticket with AWS support

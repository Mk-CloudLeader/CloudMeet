
### Route53- DNS : Private |public
-------------------------------------------------------

### LAB : Create a new private hosted zones and A record for your EC2
#### 1. Create a Domain Name : myprivatedns.com  
```
 - Select Type : Private hosted Zone|pubic hosted Zone  
	- Select VPC(s) to associate with the hosted Zone
  - You may attache many VPC, good use case for r multy aws a/c (Control tower) environments
  - Select region and VPC(s) to associate
  - Two defaults records will be created
```
#### 2.	Create “A” Record for your newly built EC2 
- Choose Routing Policy – Simple routing |weighted|Geolocation Latency|Failover|Multivalue answer 
- Define simple record :171.10.10.10  A test.myprivatedns.com
  ```
  - Record name  : test
  - Record type : “A”
  - Value/Route traffic to : 171.10.10.10
  - TTL :300
  ```
####	Outcome : Now you can access your server using hostname “A” record inside VPC to from different VPC if associated during VPC association.

####   Cloudformation to create RecordSet
```
{
   "Resources" : {
      "myDNSRecord" : {
         "Type" : "AWS::Route53::RecordSet",
         "Properties" : {
            "HostedZoneId" : "Z8VLZEXAMPLE",
            "Name" : "test.myprivatedns.com",
            "ResourceRecords" : [
               "171.10.10.10"
            ],
            "TTL" : "300",
            "Type" : "A"
         }
      }
   }
}
```
> [!TIP]
> How do I turn on reverse DNS functionality for Route 53 with a PTR record?- https://www.youtube.com/watch?v=fQ_xR40EkBQ

```
# Reverse DNS 
$ nslookup  3.23.155.245
245.155.23.3.in-addr.arpa       name = ec2-3-23-155-245.us-east-2.compute.amazonaws.com

```
The zone for reverse PTR records belong to whoever you got the IP address from
Ex : X-245.155.23.3.in-addr.arpa.
 

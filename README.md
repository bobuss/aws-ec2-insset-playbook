Quick'n'Dirty AWS EC2 playbook
---
Made during my 5 days formation on Amazon Web Service oriented on EC2 components.

What it does:
* Create a security group with :
 * INBOND : HTTP, SSH
 * OUTBOND : HTTP
* Spawn 2 **t2.micro** instances
* Add the ``public_dns_name`` to a host group
* Tag the instances
* Wait for SSH to be available on the instances
* Update the system
* Install Apache2
* Remove default ``index.html`` page and replace it by a dummy
* Wait for port 80 to be open on each instances
* Create an ELB and attach both instances to instances
* Create an AutoScaling configuration and AutoScaling group for the ELB
* Create some AutoScaling policies
* Create some AutoScaling alarms (*unfinished*)

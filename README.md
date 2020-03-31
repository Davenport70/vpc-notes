**create a vpc**

**create an internet gateway**

**attach internet gateway to vpc**

**create a private subnet**

**create a public subnet**

make sure regions are the same
ensure that ips are different

**create a route table for pub subnet**

select an internet gateway

**connect public subnet to route table**

edit subnet associations and select public subnet so it joins with the route table.

**connect private subnet to main route table**

edit subnet associations and select private subnet so it joins with the main route table.

edit subnet associations and select public subnet so it joins with the route table.

**create a public Network ACL**

edit your public inbound rules

port 80 - 0.0.0.0/0
port 443 - 0.0.0.0/0
port 22 - this one is set to my ip
port 1024-65535 range - 0.0.0.0/0

edit your public outbound rules

port 80 0.0.0.0/0
port 27017 ip 10.0.2.0/24 - whatever your public ip is.
port 1024-65535 0.0.0.0/0

**create a private Network ACL**

edit your private inbound rules

port 27017 ip 10.0.1.0/24 - whatever your private id is.
port 1024-65535 0.0.0.0/0

edit your private outbound rules

port 1024-65535 10.0.1.0/24
port 80 10.0.0.0/16

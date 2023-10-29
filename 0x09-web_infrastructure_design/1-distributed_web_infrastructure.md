# Three Server Web Infrastructure with Nginx, HAproxy, MySQL
![](https://github.com/vincent-mugendi/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/1-distributed_web_infrastructure.png?raw=true)

## Why add additional elements?

**Web server:** A web server is responsible for receiving and serving HTTP requests. By adding a second web server, we can improve scalability and reduce the risk of a single point of failure (SPOF).

**Load balancer:** A load balancer distributes traffic across multiple servers. This can improve performance and reliability. In this case, we are using HAproxy as the load balancer.

**Database cluster:** A database cluster is a group of two or more database servers that work together as a single system. This can improve performance, scalability, and availability. In this case, we are using a MySQL Primary-Replica cluster.

## Load balancer distribution algorithm

HAproxy uses a variety of load balancing algorithms, including round robin, weighted round robin, and least connections. The round robin algorithm distributes traffic evenly across all available servers. The weighted round robin algorithm distributes traffic to servers based on their weight, which can be used to give more traffic to more powerful servers. The least connections algorithm distributes traffic to the server with the fewest active connections.

### Active-Active vs. Active-Passive load balancer

An Active-Active load balancer distributes traffic across all available servers. An Active-Passive load balancer distributes traffic to a single server, with the other servers acting as backups. If the primary server fails, the load balancer will switch to one of the backup servers.

In this case, we are using an Active-Active load balancer. This is because we want to be able to handle all of the traffic that is sent to the website, even if one of the servers fails.

### Database Primary-Replica cluster

A database Primary-Replica cluster consists of two nodes: a primary node and a replica node. The primary node is the master node that stores the original data. The replica node is a slave node that is kept synchronized with the primary node.

In the event of a failure of the primary node, the replica node can be promoted to become the new primary node. This ensures that the database remains available even if one of the nodes fails.

### Differences between primary and replica nodes

The primary node is the only node that can write data to the database. The replica node can only read data from the database.

The application should only write data to the primary node. This ensures that the data is always synchronized with the replica node.

## Issues with this infrastructure

- **SPOF:** The load balancer is a single point of failure. If the load balancer fails, the website will be unavailable.
- **Security issues:** The infrastructure does not include a firewall or HTTPS. This makes the website vulnerable to attack.
- **No monitoring:** The infrastructure is not monitored. This means that problems may not be detected until they cause outages or other disruptions.

## Mitigation strategies

- **Load balancer SPOF:** To mitigate the SPOF risk, we can add a second load balancer in a high availability configuration. This means that the load balancers will be configured to monitor each other and fail over to the other load balancer in the event of a failure.
- **Security issues:** To mitigate the security issues, we can add a firewall and configure HTTPS. The firewall will protect the infrastructure from attack, and HTTPS will encrypt the traffic between the users and the website.
- **No monitoring:** To monitor the infrastructure, we can add a monitoring solution. This will allow us to detect problems early and take corrective action before they cause outages or other disruptions.

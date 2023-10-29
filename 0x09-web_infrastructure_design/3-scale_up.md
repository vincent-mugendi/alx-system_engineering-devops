## Scaled Up Web Infrastructure with HAproxy Cluster, Split Components, and Security
![](https://github.com/vincent-mugendi/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/3-scale_up.jpg?raw=true)
This web infrastructure is a scaled up version of the previous infrastructure, with all SPOFs removed and each of the major components (web server, application server, and database servers) moved to separate GNU/Linux servers. SSL protection is not terminated at the load balancer, and each server's network is protected with a firewall and monitored.

### Why split the components?

Splitting the components into separate servers makes the infrastructure more scalable and more resilient to failure. For example, if the database server fails, the web server and application server can still operate.

### Specifics

* Firewalls between each server to protect each server from unwanted and unauthorized users.

### Benefits

- **Scalability:** The infrastructure can be scaled by adding more servers to each component.
- **Reliability:** The infrastructure is more resilient to failure because the components are separated.
- **Performance: ** The load balancer can improve performance by distributing traffic across multiple servers.

### Drawbacks

* Higher maintenance costs due to the need to buy and maintain more servers, and to pay for the electricity they consume.
* Complexity: The infrastructure is more complex to manage than a one-server infrastructure.

### Comparison with Previous Infrastructure

| Characteristic | Previous Infrastructure | Scaled Up Infrastructure |
|---|---|---|
| SPOFs | Yes | No |
| Split components | No | Yes |
| SSL termination | Load balancer | Web server |
| Firewalls | Between the load balancer and the internet | Between each server |
| Monitoring | Yes | Yes |
| Scalability | Moderate | High |
| Reliability | Moderate | High |
| Security | Moderate | High |
| Cost | Low | High |

### Conclusion

Overall, the scaled up infrastructure is a good choice for websites with high traffic volumes and reliability requirements. However, it is important to be aware of the higher maintenance costs before making a decision.


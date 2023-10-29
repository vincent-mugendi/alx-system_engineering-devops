## Scaled Up Web Infrastructure with HAproxy Cluster, Split Components, and Security

This web infrastructure is a scaled up version of the previous infrastructure, with all SPOFs removed and each of the major components (web server, application server, and database servers) moved to separate GNU/Linux servers. SSL protection is not terminated at the load balancer, and each server's network is protected with a firewall and monitored.

### Specifics

* Firewalls between each server to protect each server from unwanted and unauthorized users.

### Issues

* Higher maintenance costs due to the need to buy and maintain more servers, and to pay for the electricity they consume.

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


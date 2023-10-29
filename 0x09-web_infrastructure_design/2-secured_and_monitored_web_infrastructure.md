# Three Server Web Infrastructure with Nginx, HAproxy, MySQL, and Sumologic Monitoring
![](https://github.com/vincent-mugendi/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/2-secured_and_monitored_web_infrastructure.png?raw=true)

## Why add additional elements?

**Firewalls:** Firewalls protect networks from unauthorized access. In this case, we are adding three firewalls to protect the web servers, the database server, and the load balancer.

**SSL certificate:** An SSL certificate encrypts traffic between the users and the website. This helps to protect sensitive data, such as passwords and credit card numbers.

**Monitoring clients (Sumo Logic):** Sumo Logic is a cloud-based monitoring and analytics platform that can be used to collect and analyze data from a variety of sources, including web servers, databases, and applications.

## What are firewalls for?

Firewalls are network security devices that monitor and control incoming and outgoing network traffic based on predetermined security rules. They can be used to protect networks from unauthorized access, malicious code, and denial-of-service attacks.

## Why is the traffic served over HTTPS?

HTTPS encrypts traffic between the users and the website. This helps to protect sensitive data, such as passwords and credit card numbers. HTTPS is also required for many modern web features, such as geolocation and payment processing.

## What monitoring is used for?

Monitoring is used to collect data about the performance and health of the web servers, the database server, and the load balancer. This data can be used to:

- Detect problems early and take corrective action before they cause outages or other disruptions.
- Identify performance bottlenecks and areas for improvement.
- Track trends and patterns in resource usage.
- Generate reports and dashboards for stakeholders.
- How the monitoring tool is collecting data

### Sumo Logic can collect data in a variety of ways, including:

- Polling the servers at regular intervals to collect metrics such as CPU usage, memory usage, and disk I/O.
- Listening for events from the servers, such as errors or log messages.
- Using agents that are installed on the servers to collect data.
How to monitor web server QPS with Sumo Logic

### To monitor web server QPS with Sumo Logic, you would need to collect the following metrics:

- Number of requests per second
- Number of responses per second
- Number of errors per second
- Response time
You can then use Sumo Logic's analytics tools to calculate the QPS for each web server.

## Issues with this infrastructure

1. Terminating SSL at the load balancer level: Terminating SSL at the load balancer level can reduce performance and make it difficult to troubleshoot SSL-related problems.
2. Having only one MySQL server capable of accepting writes: This is a single point of failure. If the MySQL server fails, the website will be unavailable.
3. Having servers with all the same components (database, web server, and application server): This makes the infrastructure less scalable and more vulnerable to attack.

## Mitigation strategies

- Terminate SSL at the web server level: This will improve performance and make it easier to troubleshoot SSL-related problems.
- Use a MySQL cluster: This will eliminate the single point of failure risk.
- Use separate servers for the database, web server, and application server: This will improve scalability and reduce the attack surface.

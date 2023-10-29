# Simple web stack White Board 
![](https://github.com/vincent-mugendi/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/0-simple_web_stack.png?raw=true)

# Client Request

A client/user wants to access the website www.foobar.com. Their computer sends a DNS query to resolve the domain name to an IP address. The DNS server returns the IP address of the server that hosts the website, which in this case is 8.8.8.8.

## Server Communication

The user's computer then sends a HTTP request to the GNU/Linux server at 8.8.8.8. The server receives the request and processes it. The specific steps involved in processing the request vary depending on the web server and application server being used.

In this case, the server is using Nginx as the web server and Gunicorn as the application server. Nginx is responsible for receiving and parsing HTTP requests. It then forwards the requests to Gunicorn, which is responsible for running the website code.

## Role of Each Component

- **Server:** A server is a computer that is dedicated to providing services to other computers. In this case, the server is providing the service of hosting the website www.foobar.com.
- **Domain name:** A domain name is a unique identifier that is used to address a website on the internet. In this case, the domain name is www.foobar.com.
- **DNS record:** A DNS record is a mapping between a domain name and an IP address. In this case, the DNS record for www.foobar.com maps the domain name to the IP address 8.8.8.8.
- **Web server:** A web server is a software program that is responsible for receiving and serving HTTP requests. In this case, the web server is Nginx.
- **Application server:** An application server is a software program that is responsible for running web applications. In this case, the application server is Gunicorn.
- **Database:** A database is a software program that is used to store and manage data. In this case, the database is MySQL.

## Issues

This infrastructure has a few potential issues:

- **SPOF (Single point of failure):** If the server fails, the website will be unavailable.
- **Downtime when maintenance needed:** If the server needs to be restarted or maintained, the website will be unavailable during that time.
- **Cannot scale if too much incoming traffic:** If the website receives too much traffic, the server may not be able to handle it and the website may become slow or unavailable.
Mitigation Strategies

### Some strategies that can be used to mitigate these issues include:

- Using a load balancer to distribute traffic across multiple servers: This can help to reduce the risk of a SPOF and improve scalability.
- Using a cloud-based hosting provider: Cloud-based hosting providers can offer high availability and scalability.
- Using a continuous integration and continuous delivery (CI/CD) pipeline: A CI/CD pipeline can help to automate the deployment of new code, which can reduce the amount of downtime required for maintenance.

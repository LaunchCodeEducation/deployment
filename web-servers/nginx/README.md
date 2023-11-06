## Nginx Intro

"NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers." - [Nginx Glossary](https://www.nginx.com/resources/glossary/nginx/)

The primary use that you may have for Nginx is to utilize it as a web-server. It is capable of more than just that but for now serving applications is a great start.

[Nginx Homepage](https://nginx.com)
[Nginx Documentation](https://docs.nginx.com/)
[LaunchCode Nginx Curriculum](https://education.launchcode.org/linux/web-server/nginx/setup/index.html)

DigitalOcean provides an excellent walkthrough installing and setting up Nginx on a 20.04 Ubuntu server: [DigitalOcean Nginx Walkthrough](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)

## Configuration with Nginx

NGINX is predominately driven by configuration files.

To configure NGINX to server static files, or to reverse proxy to a running web application framework NGINX requires a valid configuration file that instructs the NGINX web server on how to behave.

NGINX configuration files end with the suffix .conf.

The configuration file responsible for this NGINX web server behavior on most Linux operating systems is located at: /etc/nginx/conf.d/default.conf.

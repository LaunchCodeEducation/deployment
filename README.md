Deployment Walkthrough for Candidate Pool:

This will include an explanation of the following that leads into a walkthrough:

## What does it mean to deploy an application?

deliver service or application to the web, accessible by users

## What is required to deploy an application?

- some type of working codebase / project
- depending on codebase you will need certain dependencies on the server holding your application
Example:
  - Java/Spring application will need:
    - Java Runtime Environment
    - Source Code
    - Database if necessary
    - This is just for the application itself

## Static vs Dynamic websites

- static is pre-built or pre-defined
- dynamic is user-driven
- Examples of static websites throughout lc101, examples of dynamic (Orbit-Report, HTML Me Something, Techjobs)

## Brief Description of Linux

## Walkthrough:
- Existing Java Application (Dynamic)
- AWS EC2 + MySQL running on server and potentially RDS time permitting
- Caddy
	- tool used to serve web applications
- Ubuntu Host
	- chosen operating system for virtual machine
- ssh
	- secure shell into virtual machine to configure server
- DNS
	- domain name service to establish A record for ipv4-address
- reverse proxy
	- In this case a web user makes an HTTP request to a server. Caddy catches the initial HTTP request and passes it to a running application server. The application server processes the HTTP request and builds an appropriate HTTP response. The application server then passes the HTTP response back to Caddy who sends it back to the web user.


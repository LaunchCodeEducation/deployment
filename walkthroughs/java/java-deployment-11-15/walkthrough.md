## Launch AWS EC2 Instance
- default vpc
- Security Group (Create new)
  - allows 22 (ssh), 443 (https), and 80 (http)
- ensure that a public ipv4-address is automatically created
- Create new keypair for ssh access
- launch instance

### Server will need the following

### Deliver Jar File of Application (This is a Java/Spring application built with gradle)

The following command will create a jar file for your application:

```bash
./gradlew bootJar
```

```bash
git clone <github repo>
```

### Installations / Dependencies

- regular practice to update server upon creation (sudo apt update / sudo apt upgrade)

  - openjdk-17-jre installed to run a java environment:
    ```bash
    sudo apt install openjdk-17-jre
    ```

### mysql to connect to a database

```bash
sudo apt install mysql-server-8.0
```

  - new user created in order to access database:

    ```bash
    CREATE USER 'john'@'localhost' IDENTIFIED BY 'password';
    ```

  - database within created:

    ```mysql
    CREATE DATABASE databaseName;
    ```

### Caddy or other web-server to serve application

```bash
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list
sudo apt update
sudo apt install caddy
```

### web-server file configured
- default Caddyfile located at /etc/caddy/Caddyfile on most debian based linux distrubutions
- it is worth a note that you can create a Caddyfile anywhere on your server and reload from that location. You just nneed to ensure that its location has the ability to access to the directory of your project

  ```bash
  ipv4-address {
      reverse_proxy 127.0.0.1:running-app-port
  }
  ```

  - reload web-server:
    ```bash
    sudo caddy reload --config /etc/caddy/Caddyfile
    ```

### Configure DNS within AWS Route53

- Create new A record associated with ipv4-address of server
- update web server file and reload
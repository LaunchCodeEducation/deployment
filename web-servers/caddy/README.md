## What is Caddy?

[Caddy Homepage](https://caddyserver.com/)
[Caddy Documentation](https://caddyserver.com/docs/)
[LaunchCode Curriculum - Caddy Intro](https://education.launchcode.org/linux/web-server/caddy/setup/index.html)

"Caddy is a powerful, extensible platform to serve your sites, services, and apps, written in Go."

## Installation for Debian, Ubuntu, Raspbian

```bash
sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https
```

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg
```

```bash
curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list
```

```bash
sudo apt update
```

```bash
sudo apt install caddy
```

## Caddyfile Configuration

Caddy can be configured in multiple ways. The preferred way is by creating and managing a configuration file named Caddyfile.

The default Caddyfile file that comes with the initial Caddy installation on most Linux operating systems / distros can be located at /etc/caddy/Caddyfile.
```bash
example.com {
	root * /var/www/wordpress
	encode gzip
	php_fastcgi unix//run/php/php-version-fpm.sock
	file_server
}
```

## Caddyfile Configuration Example for Static Website

```bash
example.com {
	root * /path/to/directory/with/build-file.html
	file_server
}
```

## Caddyfile Configuration Example for Reverse Proxy

```
example.com {
	reverse_proxy ipv4-address:8080 (or whatever port your app is running on)
}
```


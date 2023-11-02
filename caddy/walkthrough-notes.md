## What is Caddy?

[Caddy Homepage](https://caddyserver.com/)
[Caddy Documentation](https://caddyserver.com/docs/)

"Caddy is a powerful, extensible platform to serve your sites, services, and apps, written in Go."

## Installation for Debian, Ubuntu, Raspbian

`sudo apt install -y debian-keyring debian-archive-keyring apt-transport-https`

`curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable-archive-keyring.gpg`

`curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/debian.deb.txt' | sudo tee /etc/apt/sources.list.d/caddy-stable.list`

`sudo apt update`

`sudo apt install caddy`

## Caddyfile Configuration

example.com {
	root * /var/www/wordpress
	encode gzip
	php_fastcgi unix//run/php/php-version-fpm.sock
	file_server
}

## Caddyfile Configuration Example for Static Website

example.com {
	root * /path/to/directory/with/build-file.html
	file_server
}

## Caddyfile Configuration Example for Reverse Proxy

example.com {
	reverse_proxy "ipv4-address:running-app-port-number" ie: 8082
}


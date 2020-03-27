#My docker-compose config

This config for laravel app

Containers:
- [Caddy server](https://caddyserver.com/) Simple web server with Let's encrypt
- PHP 7.4-latest
- Mysql 5.7

Enviorment:
``` 
cp .env.example .env
```

Help:
Caddy server response only on domains. In Caddyfile you must specify you domain, then add to /etc/hosts or Windows hosts.
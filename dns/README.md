## Intro to DNS

Domain Name Systems will be something that you will need to work with in order to configure your own server. Configuring a custom domain like "your-name.org" will first need to be purchased through a domain registrar. After your purchase the rights to the domain name you can then resolve a more "human-readable" name to your server ip-address.

There are a couple of benefits by doing such a thing:
- customization of URL
- Not exposing your ip-address
- easier access to your website

The following article provides a more in-depth guide to the topic: [DigitalOcean Domain Name System Introduction](https://www.digitalocean.com/community/tutorials/an-introduction-to-dns-terminology-components-and-concepts#conclusion)

## More on DNS / URLs

Using the following example:

```bash
https://example.launchcode.org/intro-to-web-dev-curriculum
```

We can break the URL down as follows:
- `https`: protocol (Hypertext Transfer Protocol Secure)
- `example.`: subdomain of launchcode.org
- `launchcode.`: domain name
- `.org`: TLD (Top Level Domain) - other examples include .com, .net, .gov, .edu, and .io
- `/intro-to-web-dev-curriculum`: - resource path for application

## Records

When resolving an ip-address to a domain name you need to specify what type of record will be used. For example an ipv4-address will require an `A` record and an ipv6-address will require an `AAAA` record.

There are many different types of records:
- Mail Exchanges (MX)
- Certificate Authorities (CAA)
- Alias or canonical name (CNAME)

Plus many more. Anytime you are adding a new record to an existing DNS the type of record will always be required.

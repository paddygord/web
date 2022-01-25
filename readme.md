# web

this is **not** a platform (or service, product, ...).

this is template for self-hosting a personal social website, made to be as easy as possible, and rely on as few external services/platforms as possible.

## requirements

- domain name (~£10/year from most providers)
- computer capable of running docker
- internet connection
- IPv6 support from your ISP (to bypass NAT and CGNAT complexity)

## non-requirements

- static IP (WAN or LAN). instead we use dynamic DNS via ddclient. this avoids having to talk to your ISP or configure your router.
- wired internet connection
- desktop/server form factor (laptop is fine)

this is so that it can be hosted on a windows/mac/linux wifi-connected laptop, which is pretty common and accessible.

## why?

- small marginal cost of the requirements, most people will already have access to them
- when the advertising-based internet collapses, we should have an alternative ready
- to allow and encourage a more homebrew, creative, and flexible web to flourish
- accessible in cost and complexity
- decentralisation means not relying on google/facebook/twitter, or linode/digitalocean/ovh/hetzner
- why is relying on your domain name registrar better than blockchain decentralisation? https://www.youtube.com/watch?v=YQ_xWvX1n9g
- why is this better than activitypub/mastodon? maybe because it's self-host-or-bust, rather than relying on federated hosting

## quickstart

- register your domain name ([namecheap](https://www.namecheap.com) seems to work well for this)
- edit `avagordon.name` in `docker-compose.yml` to your domain name
- [install docker](https://docs.docker.com/get-started/)
- `docker compose up -d`
- edit `ddclient/ddclient.conf` to put in your domain name and dynamic DNS password from your domain registrar

## content

modify the files in `./swag/www/`, and/or put other `.html`, `.css`, `.js` files in there too.

your main page should be called `index.html`

## legal and moderation

everything is owned, hosted, and/or registered by the individual. so they are responsible for the legality of the hosted content.

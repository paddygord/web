# web

this is **not** a platform (or service, product, ...).

this is a guide to self-hosting a personal social website, made to be as easy as possible, and rely on as few external services/platforms as possible.

## requirements

- domain name (~£10/year from most providers)
- computer capable of running docker
- internet connection

## non-requirements

- static IP (WAN or LAN). instead we use dynamic DNS via ddclient. this avoids having to talk to your ISP or configure your router.

## quickstart

- register your domain name ([namecheap](https://www.namecheap.com) seems to work well for this)
- edit `avagordon.name` in `docker-compose.yml` to your domain name
- [install docker](https://docs.docker.com/get-started/)
- `docker compose up -d`
- edit `ddclient/ddclient.conf` to put in your domain name and dynamic DNS password from your domain registrar

## content

modify the files in `./swag/www/`, and/or put other `.html`, `.css`, `.js` files in there too.

your main page should be called `index.html`

## mostly static?

this is to enable discovery of other self-hosted websites while minimising reliance on a centralised platform.

the website is configured by default to set a cookie that gives the URL of your website to others when you visit their website.

TODO is this technically possible?
- https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie/SameSite
- https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/cookies#first-party_isolation
- https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy

## legal and moderation

everything is owned, hosted, and/or registered by the individual. so they are responsible for the legality of the hosted content.

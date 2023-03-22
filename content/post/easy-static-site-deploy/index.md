---
title: Not so easy private static site deploy
description: Instructions on how to create project documentation with private access
slug: static-site-deploy
date: 2023-01-03 00:00:00+0000
image: img.png
draft: true
categories:
- Guide
tags:
- Docs
- Tools
- Static sites
- Infrastructure
---

That's easy to find hosting for your public static site blog.
There is a plenty of services such as AWS Amplify, CloudCannon, Cloudflare Pages, GitHub Pages, GitLab Pages, Vercel and Netlify.

Many of them is free.

But things is harder, then it comes to private site.
Internal documentation, internal company blog or closed community site.

## Expensive

Many static site hosting solutions allows to create website under authorization.

### Git Pages

Gitlab pages, github pages

#### Downside

Enterprise payment plans are too expensive for startups.
On other side per member payment plans are too expensive for enterprise.
Because there is a lot of people that

### Static hosting services

Vercel, Netlify

cloudcannon.com Good tool that gives CMS and hosting experience for static sites.
Also, it has site user authentication options.

## Free, but requires familiarity with CLI

You can set up web server using opensource tools. 

### Requirements

But you need some skills (or enough motivation to learn it now by yourself):
- Experience or motivation to buy domain name and connect it to server IP address
- Linux CLI usage
- Docker (in case of problems)

If you have no experience in it. You'll need 40-80 hours to get through.

### Steps

1. Google and choose cloud VPS provider. Or just go to popular DigitalOcean.
2. Find system image with preinstalled docker and docker-compose. [Example](https://marketplace.digitalocean.com/apps/docker).
3. Create server with this image.
4. Choose domain name, buy it and setup DNS to your server ip address.
5. Use command line for ssh connection to server.
6. Create `docker-compose.yml` file with content from this gist
7. Create `.env` file with this gist. Paste your domain name and secrets. `{}` should be deleted.
8. Run `docker-compose up`
9. Go to admin.yourdomain.name. Sign in with admin credentials. Create bucket and upload website files.
10. Go to yourdomain.name/bucketname. Sign in with viewer credentials. Page should show.

That's it. 
After this steps you must have documentation site and admin UI for uploading new files.

{{<columns>}}
***Change credentials every month for better security***
<--->
***Use minio S3 compatible API to automate uploading***
{{</columns>}}


## 1$ is all I need

I see price and skill barriers.
Newcomers and not programming specialists have not simple way to create private documentation site.

I decided to create service without these barriers.

---
title: "Hugo Themes as Modules"
date: 2023-05-09T21:24:55+02:00
draft: false
---

Hugo now has [modules](https://gohugo.io/hugo-modules/). These are core building blocks, and they include themes. We're going to look at how to use this new feature.

## Prerequisites
To use modules with Hugo, we need to have the following installed:
- [Hugo](https://gohugo.io/installation/) - latest **extended** version.
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Go](https://go.dev/doc/install)

### Create a new site
Let's start with a blank slate. Run the following in your terminal:
```bash
hugo new site hugo-module-theme
cd hugo-module-theme

git init

# Hugo modules depend on Go modules.
# This is the repo I'm using to hold this code.
# You can use your own.
go mod init github.com/17xande/hugo-module-theme
```

### Pick a theme
You can browse an extensive collection of themes at <https://themes.gohugo.io>.  
Here are a few themes that are built using Hugo modules:

- [Anubis](https://themes.gohugo.io/themes/hugo-theme-anubis/)
- [DocuAPI](https://themes.gohugo.io/themes/docuapi/)
- [Nightfall](https://themes.gohugo.io/themes/hugo-theme-nightfall/)
- [Terminal](https://themes.gohugo.io/themes/hugo-theme-terminal/)

We're going to pick Anubis for this tutorial.  
At this time, there seem to be multiple ways to use a Theme module. If you read the instructions for each of those themes you will see they all differ slightly, but they all seem to work.

My faviourite way, because it's the simplest way, is to add the following to the `config.toml` file:
```toml
theme = ["github.com/Mitrichius/hugo-theme-anubis"]
```
### Start your Hugo server
The hard part is over, now you can just start your hugo development server, and it will take care of the rest:
```bash
hugo server
```
You should see something like the following:
```
go: no module dependencies to download
hugo: downloading modules …
go: downloading github.com/Mitrichius/hugo-theme-anubis v0.0.0-20230505192016-a9272e10f062
go: added github.com/Mitrichius/hugo-theme-anubis v0.0.0-20230505192016-a9272e10f062
hugo: collected modules in 2552 ms
Start building sites …
...
Web Server is available at http://localhost:1313/
```

## Voila!
You now have a Hugo website that uses a Hugo module theme. Simple and easy.

In the next post, we'll be looking at deploying this site to the Internet, by hosting it on [Netlify](https://www.netlify.com/).

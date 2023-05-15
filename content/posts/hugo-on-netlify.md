---
title: "Hugo on Netlify"
date: 2023-05-15T12:02:36+02:00
draft: true
---

We're going to deploy [our simple Hugo site](/posts/hugo-themes-as-modules) to Netlify.

Let's start with installing the [Netlify CLI](https://docs.netlify.com/cli/get-started/):
```bash
npm install netlify-cli -g

# Run the command to make sure it installed correctly:
netlify

# ⬥ Netlify CLI
# Read the docs: https://docs.netlify.com/cli/# # get-started/
# Support and bugs: https://github.com/netlify/# cli/issues
# ...
```
Authenticate netlify-cli:
```bash
netlify login
```
This will open a browser window, asking you to log in with Netlify and grant access to netlify-cli.

Connect your repository to run a continuous deployment from github:
```bash
netlify init
```
This will prompt you to login to your github account, and for you to grant Netlify access to your repository for the CI builds.



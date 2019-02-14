---
title: 2. Your first article from Git repository
tags: ["GitPress", "GitPressTutorial"]
date: 2018-12-31
---

**GitPress** uses Git to sync articles. So you can the tools of development to publishing articles.

The flow is very simple:

1. You need to prepare a public Git repo at GitHub
2. [Login to GitPress](https://gitpress.io/login), and setup article repository at settings.
3. To keep your articles synced, add a webhook at GitHub to notify GitPress when something changes.
4. Now, you can compose articles now. Any push to master branch will sync the articles to GitPress automatically.

## Prepare a Git repository

You need a Git repository to contains your articles files. Go to [Github](https://github.com/new), create a new repository.

1. You can use any repository name. For example, `my-blog`.
2. Choose the **Public** permission options to make sure the repository is visible to the public.
3. Tap `Create repository`.

## Setup article repository

[Login to GitPress](https://gitpress.io/login), and you will land to your profile page with empty article list.

1. Tap `settings` to setup articles
2. Add the **Article Repo Url** from the repo you are created at last step. Please use the HTTPS version. For example, `https://github.com/{YOUR_GITHUB_NAME}/my-blog.git`.
   - If your articles are placed in a directory, please specify the path at **Directory**. For example, `/source`
3. Copy the **Webhook Url**

## Add a webhook to keep your articles alive

Webhook is a simple way to notify GitPress if you change something in Git repo.

1. Visit your Github repo settings(`settings - webhooks`)
2. tap the `Add webhook` button
3. Paste the Webhook Url you copied at last step
4. Choose `application/json` at content type options
5. Tap the green `Add Webhook` button

## Compose and commit your first article

All done. Now you can add a new Markdown file at repo, write something, commit and push. All changes will by sync to GitPress automatically.

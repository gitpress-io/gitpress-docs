---
title: 2. Your first article from GitHub Repo
tags: ["GitPress", "GitPressTutorial"]
date: 2018-12-31
---

**GitPress** uses Git to sync articles. So you can use the tools of development for publishing.

1. You need to prepare a GitHub repo.
2. [Login to GitPress](https://gitpress.io/login) via Github account, select the repository.
3. To keep your articles synced, GitPress will ask for adding a webhook at GitHub get notified when something changes.
4. Now, you can compose articles now. Any changes at master branch will sync the articles to GitPress automatically.

## Prepare a GitHub repo

You need a GitHub repository to contains your articles files. Go to [Github](https://github.com/new), create a new repository.

1. You can use any repository name. For example, `my-blog`.
2. Choose the **Public** permission options to make sure the repository is visible to the public.
3. Tap `Create repository`.

## Choose a repo

[Login to GitPress](https://gitpress.io/login). Choose a repository which contains your articles.

![Onboarding](/first-article/onboarding.jpg)

## Setup article repo

GitPress uses webhook to sync content from GitHub. You'll be asked for a permission to add a webhook.

In addition, if you choose a private repo, you'll be asked for a permission to add a deploy key in this step.

![Almost done](/first-article/almost-done.jpg)

Tap "Allow" to complete setup.

## Compose and commit your first article

All done. Now you can add a new Markdown file at repo, write something, commit and push. All changes will be synced to GitPress automatically.
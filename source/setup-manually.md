---
title: Setup your repos(public and private) to sync with GitPress
tags: ["GitPress", "GitPressHelp"]
date: 2019-02-22
---

**Important: not supported yet. I will implement it ASAP**

It's fine if you skip the onboarding guide and prefer to setup repo manually. 

To setup manually is also the recommended way to sync with private repos.

## Sync Public Repo

### Setup Repo Url

On your repo's settings page, copy the HTTPS based Git Url. For example, `https://github.com/gitpress-io/blog`

Back to GitPress, visit article's settings page or collection's setting page. Tap "Other repos" link beside Repo dropdown, paste the Url.

Tap "Save" button.

### Add Webhook

On your repo's settings page, copy the Webhook Url

Visit your private repo's webhook settings page at GitHub, Tap "Add webhook"

Fill the Url entry, and Tap the green button "Add webhook" at bottom of the form.

### Rebuild

On your repo's settings page, Tap "Rebuild" button


## Sync Private Repo

By default, GitPress can't access your private repos.

If you want to use private repo as posts source, you need to follow the instructions above to manually setup and do an additional step to complete.

### Setup Repo Url

Because GitPress can't read private repos, you should tell GitPress which private repo you are want to use. See the instruction aboved.

Note: the Repo Url of private repo should begin with `git@`. For example, `git@github.com:gitpress-io/private-blog.git`

### Add Webhook

GitPress has no permission to create webhook on your private repos, you have to add webhook your self. See the instruction aboved.

### Add Deploy Key

To read the content in your private repo, GitPress is asked for a deploy key.

GitPress has generated a deploy key at settings page for each private repo. Copy it and visit your private repo's deploy key page, tap "Create deploy key".

Fill the form: paste the key into the textarea, and type a name for the key.

Tap "Create deploy key".


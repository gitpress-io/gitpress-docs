---
title: Frequently asked questions(FAQ)
tags: ["GitPress", "GitPressTutorial"]
date: 2018-12-31
---

**Q: Do you have an online editor?**

A: No.

GitPress doesn't offer any online editor because we think standalone Markdown editor will do a better job for you.

You can use any editor you like to compose your articles. In additional, GitPress uses Git to sync content, you can use
Github's online editor to write your articles.

**Q: How many programming languages do you support?**

A. Benefit from [Code Mirror](https://codemirror.net), GitPress supports the powerful, composable language mode system 
for [over 100 languages](https://codemirror.net/mode/index.html) out of the box.

**Q: Which programming languages can I run in the article?**

A: By now, GitPress supports 5 languages to run inline, they are Javascript, Python 2, Ruby, C/C++, Scheme.
We are still working on more language playgrounds. Check [the language support](languages).

**Q: How to upload images and pictures?**

A: I recommend you to keep image files or pictures in an online image sharing and host service like imgur, google cloud, Amazon S3, etc.
However, if you place image files in the article repo, it's fine. GitPress will handle and render them properly.
You should place them in a directory with same name as your article. 

For example:

You mention a picture in Markdown file `abc.md`:

```markdown

![An image](/abc/sample.jpg)

```

You should make sure `sample.jpg` is in the directory named `abc`


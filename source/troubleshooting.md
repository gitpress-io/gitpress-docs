---
title: Troubleshooting
tags: ["GitPress", "GitPressHelp"]
date: 2019-02-14
---

## Troubleshooting

### GitPress can't find articles

Please follow the instructions to check your settings:

1. the **Article Repo Url** is correct and can be access by GitPress.
2. the **Directory** of Article Repo Url is correct. By default, it's `/`.
3. all articles are placed in the **Directory** without any sub directory.
3. all articles end with ".md" or ".markdown" extension.
4. all articles should have [front-matter](front-matter) at begining of file.

Check out [GitPress logs](https://github.com/gitpress-io/blog) to learn about the directory structure.

It's settings are:

- **Address**: https://gitpress.io/@gitpress
- **Article Repo Url**: https://github.com/gitpress-io/blog.git
- **Directory**: /source

### Collection has no table of content

GitPress uses `TOC.md` file to generate table of content for each collection.

Please follow the instructions:

1. There is a `TOC.md` file be placed in the collection path.
2. The content of `TOC.md` is correct. For more about the specification, [read here](collection-toc).

### GitPress can't find collection articles

Please follow the instructions to check your settings:

1. the **Github Repo Url** is correct and can be access by public.
2. the **Repo Directory** of Article Repo Url is correct. By default, it's `/`.
3. all articles are placed in the **Repo Directory** without any sub directory.
3. all articles end with ".md" or ".markdown" extension.
4. all articles should have [front-matter](front-matter) at begining of file.

GitPress Help is a regular collection. Check out [it's source here](https://github.com/gitpress-io/gitpress-docs]).

It's settings are:

- **Address**: https://gitpress.io/c/helps
- **Github Repo Url**: https://github.com/gitpress-io/gitpress-docs.git
- **Repo Directory**: /source

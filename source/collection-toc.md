---
title: 3.2 Use table of content
tags: ["GitPress", "GitPressTutorial"]
date: 2018-12-31
---

GitPress uses a regular Markdown file as the table of content, which named `TOC.md`.

To enable the table of content for collection, you should put `TOC.md` under the Repo Directory.

Assume your article directory is `src/`, then the repo structure should be:

```bash
/ 
    /src
        TOC.md
        file1.md
        file2.md
        ... 
```

## The constructor of `TOC.md`

TOC.md is built by several section and list.

You can use HEADING prefix `#` to start a section and use unorder list to arrange the table of content.

Each list should be a link to filename without '.md' extension. For example, this file named `welcome.md`, you can specify `welcome` as the link.

## Example: the `TOC.md` file of this collection

```markdown
# Getting Started

- [1. Welcome to GitPress](welcome)
- [2. Your first article from Git repository](first-article)
- [3. Use GitPress Collections](collection)
    - [3.1 Create a collection](create-a-collection)
    - [3.2 Use table of content](collection-toc)
- [4. FAQ](faq)

# User Manual

- [Front matter specification](front-matter)
- [Supported languages](languages)
```

Enjoy.

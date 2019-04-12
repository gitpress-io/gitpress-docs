---
title: Markdown for GitPress
tags: ["GitPress", "GitPressHelp"]
date: 2019-04-01
---

## Overview

[John Gruber](https://en.wikipedia.org/wiki/John_Gruber) and [Aaron Swartz](https://en.wikipedia.org/wiki/Aaron_Swartz) created the Markdown language in 2004, with the goal of enabling people "to write using an easy-to-read and easy-to-write plain text format"

There are varies syntax between different parsers, **GitPress** is using [marked.js](http://marked.js.org/).

## Block Elements

### Paragraph and line breaks

A paragraph is simply one or more consecutive lines of text. In markdown source code, paragraphs are separated by two or more blank lines. In GitPress, you only need one blank line to create a new paragraph.

### Headers

Headers use 1-6 hash (`#`) characters at the start of the line, corresponding to header levels 1-6. For example:

``` markdown
# This is an H1

## This is an H2

### This is an H3
```


### Blockquotes

Markdown uses email-style > characters for block quoting. They are presented as:

``` markdown
> This is a blockquote with two paragraphs. This is first paragraph.
>
> This is second pragraph. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> This is another blockquote with one paragraph. There is three empty line to seperate two blockquote.
```

### Lists

Input `* list item 1` will create an unordered list - the `*` symbol can be replace with `+` or `-`.

Input `1. list item 1` will create an ordered list - their markdown source code is as follows:

``` markdown
## un-ordered list
* Red
* Green
* Blue

## ordered list
1. Red
2. Green
3. Blue
```

### Task List

Task lists are lists with items marked as either [ ] or [x] (incomplete or complete). For example:

``` markdown
- [ ] a task list item
- [ ] list syntax required
- [ ] normal **formatting**, @mentions, #1234 refs
- [ ] incomplete
- [x] completed
```

### Code Blocks

GitPress uses [Code-Knack](https://github.com/lyricat/code-knack) as the living code evaluator. For supported languages, we'll run it through syntax highlighting and executable:

``` markdown
Here's an example:

​```
function test() {
  console.log("notice the blank line before this function?");
}
​```

syntax highlighting:
​```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
​```
```

You can find more details [here](https://gitpress.io/@gitpress/languages).


### Diagrams and LaTeX

You can render *LaTeX* mathematical expressions and Diagrams using Code block;

```latex
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
```

You can find more details [here](https://gitpress.io/@gitpress/diagrams-with-mermaid) and [here](https://gitpress.io/@gitpress/latex).

### Tables

In markdown source code, tables look like:

``` markdown
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
```

You can also include inline Markdown such as links, bold, italics, or strikethrough in the table.


### Horizontal Rules

Inputting `***` or `---` on a blank line and pressing `return` will draw a horizontal line.

------

### YAML Front Matter

GitPress now supports [YAML Front Matter](http://jekyllrb.com/docs/frontmatter/). 

You can find more details [here](front-matter)


### Table of Contents (TOC)

TOC will be generated automatically for each article.

### Message Blocks

GitPress implement some Markdown extension from [Open Publishing Service](https://docs.microsoft.com/en-us/contribute/how-to-write-use-markdown#ops-custom-markdown-extensions), such as Message Blocks.

You can choose from several types of message blocks to draw attention to specific content:

- NOTE
- WARNING
- ERROR
- TIP
- IMPORTANT

Examples:

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!ERROR]
> This is a ERROR

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

These render as follows:

> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!ERROR]
> This is a ERROR

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT


## Span Elements

### Links

Markdown supports two styles of links: inline and reference.

In both styles, the link text is delimited by [square brackets].

To create an inline link, use a set of regular parentheses immediately after the link text’s closing square bracket. Inside the parentheses, put the URL where you want the link to point, along with an optional title for the link, surrounded in quotes. For example:

``` markdown
This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
```

will produce:

This is [an example](http://example.com/"Title") inline link. (`<p>This is <a href="http://example.com/" title="Title">`)

[This link](http://example.net/) has no title attribute. (`<p><a href="http://example.net/">This link</a> has no`)

#### Internal Links

**You can set the href to headers**, which will create a bookmark that allow you to jump to that section after clicking. For example:

Command(on Windows: Ctrl) + Click [This link](#block-elements) will jump to header `Block Elements`. To see how to write that, please move cursor or click that link with `⌘` key pressed to expand the element into markdown source.

#### Reference Links

Reference-style links use a second set of square brackets, inside which you place a label of your choosing to identify the link:

``` markdown
This is [an example][id] reference-style link.

Then, anywhere in the document, you define your link label on a line by itself like this:

[id]: http://example.com/  "Optional Title Here"
```

In GitPress, they will be rendered like so:

This is [an example][id] reference-style link.

[id]: http://example.com/	"Optional Title Here"

The implicit link name shortcut allows you to omit the name of the link, in which case the link text itself is used as the name. Just use an empty set of square brackets — for example, to link the word “Google” to the google.com web site, you could simply write:

``` markdown
[Google][]
And then define the link:

[Google]: http://google.com/
```

In GitPress, clicking the link will expand it for editing, and command+click will open the hyperlink in your web browser.

### URLs

GitPress allows you to insert URLs as links, wrapped by `<`brackets`>`.

`<i@GitPress.io>` becomes <i@GitPress.io>.

GitPress will also automatically link standard URLs. e.g: www.google.com.

### Images

Images have similar syntax as links, but they require an additional `!` char before the start of the link. The syntax for inserting an image looks like this:

``` markdown
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
```

You can find more details [here](faq).

### Strong

A double `*` or `_` will cause its enclosed contents to be wrapped with an HTML `<strong>` tag, e.g:

``` markdown
**double asterisks**

__double underscores__
```

output:

**double asterisks**

__double underscores__

GitPress recommends using the `**` symbol.

### Code

To indicate an inline span of code, wrap it with backtick quotes (`). Unlike a pre-formatted code block, a code span indicates code within a normal paragraph. For example:

``` markdown
Use the `printf()` function.
```

will produce:

Use the `printf()` function.

### Strikethrough

To create strikethrough text, round your text with `~~`.

`~~Mistaken text.~~` becomes ~~Mistaken text.~~



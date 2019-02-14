---
title: Front Matter Specifications
tags: ["GitPress", "GitPressHelp"]
excerpt: Explaination of front-matters, settings and default values supported by GitPress.
date: 2018-12-31
---

**Front-matter** is a block of YAML at the beginning of the file that is used to configure settings for your writings. Front-matter is terminated by three dashes when written in YAML.

```yaml
---
title: Hello World
date: 2013/7/13 20:46:25
---
```

## Settings & Default Values

| Setting	| Description	| Default |
| --- | --- | --- |
| title	| Title	 | **required** |
| date	| Published date	| Article created date |
| tags	| Tags 	 | `[]` |
| excerpt | Excerpt | "" |

### Example: the front-matter of this article

```yaml
---
title: Front Matter Specifications
tags: ["GitPress", "GitPressHelp"]
excerpt: Explaination of front-matters, settings and default values supported by GitPress.
date: 2018-12-31
---
```


# duality-community.github.io

**Welcome to the Community Site repository of the Duality game engine!**

## About
This site is brought to you by the small, yet awesome community of the Duality game engine.
Its purpose is to gather the lasting community content related to the engine, and also to host and encourage the production of such content.
Also it is intended to serve as a feed of news about the development of the engine, community plugins, and games created with Duality.

This means, that every user of the engine *(including YOU)* is very welcome to contribute to the site.

## What to contribute

New articles are always welcome! Topics can vary greatly and are not limited to Duality-specific areas either. If you want to contribute, but are not yet sure which topic to pick, here are some ideas:

* A small-but-nice feature you made
* How to render something that is not a sprite
* A useful code snippet
* An article about a game you're making
* A quick introduction of a game jam that will start soon
* Where you get your game resources
* Five ways to organize your game resources, with pros and cons
* What you learned when making your last game
* ...and so on!

Of course you can also submit Pull Requests with small edits and adjustments, like fixing a typo here and there, or rewriting a smaller part of a page.

## How to contribute
The project is built upon the technology provided by [Jekyll](https://jekyllrb.com) and [GitHub Pages](https://pages.github.com).
Although both of them features comprehensive documentation, here stands a quick list of instructions aimed at beginners to catch up as quickly as possible.
It requires nothing but a GitHub account and a web browser.

1. Fork this repository to your GitHub account.
2. In your newly created repository, under the *Code* tab, navigate to the `_posts` folder.
3. Click `Create new file`
4. Name your file accordingly: the required format is `YYYY-MM-DD-title.md` (For example: 2017-09-01-introduction.md)
5. Copy the following lines to the beginning of the new file. It is called 'front matter', and contains meta-information related to the new article.
```
---
layout: post
title:
date:
categories:
tags:
author:
---
```
6. Fill the `title`, `date`, `categories`, `tags` and `author` fields accordingly
  - `title` and `author` should be obvious,
  - `date` should have the format `YYYY-MM-DD`
  - check the site for the available [`categories`](https://duality-community.github.io/category/)
    and [`tags`](https://duality-community.github.io/tag/) or you can add new ones as well
7. Write the article about your newly discovered hack / game shipped with Duality / tutorial. *(This step is important!)*
8. Open a pull request to the original repository (this)
11. Wait for the site's maintainers review your article. After they approved and merged it, your article shows up on the site.

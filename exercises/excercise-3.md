# Exercise 3: Raise a pull request and publish your outline

The aims of this exercise are to familiarize you with the process of:
- making a contribution to a public GitHub repo
- using a static site generator (in this case Jekyll) to render it

Whilst not all publications operate in this way this exercise will you equip you with the key skills to publish blogs to those that do and will introduce many of the key concepts necessary to complete [challenge 2](../challenges/challenge-2.md).

> Before you start: this is a much longer exercise than the previous two, don't worry if you don't finish it in the workshop time. You can still follow the steps below and complete this exercise after the session.

## What is a PR?

A pull request is a way of requesting that the maintainers of a repo "pull" your code changes into their main branch. In this exercise we will use a PR to add your blog outline [to this blog feed](https://notanother.pizza/blog-workshop/) on the [notanother.pizza](https://notanother.pizza) website.

## Instructions 

1. Fork the [notanother.pizza/site repo](https://github.com/notanotherpizza/site) by navigating to and clicking the "fork" button on the top right of the page. 

> "Forking" a repo creates a copy of the upstream repo (in this case notanotherpizza/site) that you can make changes to, later on you can contribute these changes back to the upstream branch via a PR, this process saves the maintainers from having to individually grant access to would be contributors and means anyone can suggest changes. This basic process underpins most open-source contributions. Neat!

![Create fork button](../images/new-fork.png)

You can leave all the settings as the defaults and click "Create Fork".

![Creating a fork of the repo](../images/create-new-fork.png)

2. Create a codespace which will allow you to edit the repo in your browser (this can take a few minutes).

![Creating a github codespace from a fork](../images/create-codespace.png)

3. Create a new branch by copy pasting the following into the terminal at the bottom of the codespace and pressing enter.

```bash
git checkout -b yourname-workshop
```

> Hint: Now is a good time to open your newly cloned repo in VS Code to make the next steps easier.

4. Create a new Markdown (.md) file in the `_posts` directory with today's date and the title of your blog, for example: `2025-04-15-Not-Another-Update.md` `yyyy-mm-dd-your-blog-title.md`.

5. Copy your outline from [exercise 2](../exercises/excercise-2.md) into your newly created file.

6. At the beginning of your file add the following tags so that Jekyll can render the page correctly.

```
---
layout: post
title: Example Outline
author: your-name
category: workshop
---

*your outline*
```

> Optional: run jekyll locally to see what your outline looks like rendered before you merge them, for instructions on how to do this [see the docs for the Jekyll template here](https://github.com/notanotherpizza/site/blob/main/jekyll-mono.md#local-development).

7. Commit your changes to your local branch and push to the remote branch with:

```bash
git add .

git commit -m "Workshop date"

git push -u origin yourname-workshop
```

8. Back in GitHub create a PR and select merge to notanotherpizza/main by navigating to the Pull Request tab and clicking "New".

![](../images/new-pr.png)

In the create PR screen select the notanotherpizza/main branch as the target and your newly created branch as the source and click "Create Pull Request"

![](../images/create-pr.png)

9. Wait for it to be approved, [ping a maintainer](https://github.com/hevansDev/site?tab=readme-ov-file#maintainers) to expedite this process. Once it's approved you can click the "Merge" button the PR merge your changes to the remote and add your changes to the repo.

10. Once your changes are merged to notanotherpizza/main the Jekyll GitHub action will create render the changes and update the GitHub pages website. You should be able to see your published outline at https://notanother.pizza/blog-workshop/!

## Next Steps

Congratulations on successfully publishing your outline and completing the beginners blog workshop. If you enjoyed this session why not try [challenge 1](../challenges/challenge-1.md) complete your blog, and then use the process above to update your outline into a finished blog?

Once you've done that you can always try [challenge 2](../challenges/challenge-2.md) hosting your own blog on GitHub pages.


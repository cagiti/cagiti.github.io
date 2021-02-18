---
author: Cai Cooper
title: "Cloud Native bits 'n bytes"
subtitle: 
description: 
tags:
  - cloud-native
  - tools
  - developer
categories:
  - cloud-native
  - tools
aliases:
  - bits-n-bytes
---

What is this? Hopefully this is not another list of tools that aren't useful. I thought it might be useful to compile a list of commands/packages I've found useful when interacting with the various technologies. I will do my best to keep it up to date... pull requests are welcome ;)! Let's start at the beginning:

## [git](https://git-scm.com/)

There are far too many useful `git` command, here's some I've found useful.

### [git add -p](https://git-scm.com/docs/git-add#Documentation/git-add.txt--p)

I've personally found this command a life saver, and not as popular as I'd expect. If you've found yourself making too many types of changes for a single commit or you'd prefer to review your changes interactively, this command is for you. This command allows you interactively select hunks of your change into your changeset, really useful... especially when pairing.

### [git push --force-with-lease](https://git-scm.com/docs/git-push#Documentation/git-push.txt---force-with-leaseltrefnamegt)

This has been extremely useful when you've found that you've needed to amend a commit, using `--force` obliterates the git history which isn't great... `--force-with-lease` for the win.

## [gh](https://github.com/cli/cli)

A cli for GitHub.

### [gh repo fork <owner/repo> --clone --remote](https://cli.github.com/manual/gh_repo_fork)

Needs little explanation:
- forks the repository (is idempotent)
- clones the repository
- sets origin & upstream (origin=fork, upstream=remote)

### [gh repo view](https://cli.github.com/manual/gh_repo_view)

Anywhere in the repo, view the README.

### [gh release download --repo \<repo\> -p "\<pattern\>"](https://cli.github.com/manual/gh_release_download)

Dowload releases from github repositories, `gh release download --repo plumming/dx -p "*darwin*"` - this will download that latest release of the package matching the `*darwin*` pattern.

_More coming soon..._

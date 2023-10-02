---
title: "Hello World"
date: 2023-06-01 00:00:00 +0800
categories: [Hello World]
tags: [Hello World]
---

# Hello Woorld

Hello World this is the RTS Developer Guide.

Update the variables of `_config.yml`{: .filepath} as needed. Some of them are typical options:

- `url`
- `avatar`
- `timezone`
- `lang`

Go to the root of the source project, and build your site as follows:

```console
$ JEKYLL_ENV=production bundle exec jekyll b
```


#### Option 2. GitHub Fork

Sign in to GitHub to [fork **Chirpy**](https://github.com/cotes2020/jekyll-theme-chirpy/fork), and then rename it to `USERNAME.github.io` (`USERNAME` means your username).

Next, clone your site to local machine. In order to build JavaScript files later, we need to install [Node.js][nodejs], and then run the tool:

```console
$ bash tools/init
```

> If you don't want to deploy your site on GitHub Pages, append option `--no-gh` at the end of the above command.
{: .prompt-info }

The above command will:

1. Check out the code to the [latest tag][latest-tag] (to ensure the stability of your site: as the code for the default branch is under development).
2. Remove non-essential sample files and take care of GitHub-related files.
3. Build JavaScript files and export to `assets/js/dist/`{: .filepath }, then make them tracked by Git.
4. Automatically create a new commit to save the changes above.

### Installing Dependencies

Before running local server for the first time, go to the root directory of your site and run:

```console
$ bundle
```
---
title: Starting A Blog Hosted On Github Pages
date: 2023-10-01 20:14 +0300
categories: [Blogging, Tutorial]
tags: [github-pages, blog, personal blog, jekyll]
---

## My first ever blog post

I've been thinking about starting a blog for a while now and I was procrastinating quite a bit :D. But, I finally did it and here I am writing my first ever blog post. Suprisingly enough, it will be about my experience setting up my blog and how you can do it too :D.

![Desktop View](/assets/img/post-2023-10-02-starting/Intro_meme.jpg){: width="500"}
_Scenario of a developer starting a blog_

### [YouTube Video Walkthrough](https://youtu.be/m1RYsmOMPLs)

## Why Github Pages?

I'm a progammer. I've always wanted to have a personal website to showcase my projects and share my thoughts. I've looked into various blogging platforms like [Wordpress](https://wordpress.com/), [Medium](https://medium.com/), [Substack](https://substack.com), and [Ghost](https://ghost.org/). But, I chose Github Pages with Jekyll because I wanted to have:
1. Full control over my blog and I wanted to customize it to my taste. 
2. A blog that is free and doesn't require me to pay for hosting. 
3. A blog that is simple, fast and easy to maintain doesn't require me to spend hours to configure it.

Did I convince you? OK, now let's break down the steps to setup your blogging site.

## Step 1: Decide Your Theme

This step is to quickly browse through the various Jekyll themes available on various websites and pick one that fits your taste



## Step 2: Activate Github Pages

Once you pick the Jekyll theme, it's time to host it on Github Pages. The theme you picked usually comes with a set of instructions to configure and the instruction varies between different themes.

For Chirpy theme, the instructions are as follows:
1. Use the  to create your own repository.
    - Make sure to name it as `<your-gh-username>.github.io`
    - After doing this step Github actions will build and deploy your blog automatically to `<your-gh-username>.github.io`
    - But you don't want just a template, you want to customized it to yourself. So, let's move on to the next step.
2. Clone the repository you just created.


## Step 3: Setup Your Custom Root Domain

You need to visit one of the domain name registrar to buy a custom domain. There are multiple registrars to choose from: 


*I personally chose GoDaddy since I had to pay ~10$ for 2-years plan*

### Configure Your Domain

After you purchase your domain, go into your domain management portal, click on manage DNS and add `A` type DNS records for github pages.

| Type | Data |
|------|------|
| A | 185.199.108.153 |
| A | 185.199.109.153 |
| A | 185.199.110.153 |
| A | 185.199.111.153 |
| CNAME | gh-username.github.io |

*(These `A` type DNS records map your domain name to the Github's IP address)*


So far, my DNS record looks like this:

### Configure Github Pages

Now that you have your domain's DNS setup, Let's head back to Github and configure your Github Pages to use your custom domain.


## Bonus Tip: Test Your Site

If you see a `404 error` or `Domain Not Found error` your DNS record might not be updated. Every time you update a DNS record, it takes few mins to several hours to propagate the WWW. So, give it sometime. To see if your domain is reachable, you could dig the DNS:

```bash
$ dig YOUR-DOMAIN.COM +noall +answer
```

Here is a reference from digging my website:

```bash
$ dig ahmedtremo.com +noall +answer
ahmedtremo.com.    0    IN    A    185.199.111.153
ahmedtremo.com.    0    IN    A    185.199.109.153
ahmedtremo.com.    0    IN    A    185.199.110.153
ahmedtremo.com.    0    IN    A    185.199.108.153
```

Hope you found this article useful. If you have any questions, you can check my [LinkedIn](https://www.linkedin.com/in/nahuel-retes/).


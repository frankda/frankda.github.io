---
title: Use Jekyll Create GitHub Page (For Windows)
description:
categories:
 - A Guide for start coding
tags:
---

## Intro

My GitHub page has been built in one month. During this process, I started from knowing nothing about coding and solved a lot of difficulties by using Google. Finally, my blog was set up as frankda.github.io

As my memory is still fresh, I will write down the whole process of how I build my GitHub Page.

Following this article, you can also build your own Github page like mine: https://frankda/github.io



## Build a personal blog

We will use Jekyll to generate a website and put it on Github page.



### Set up a new Github project

1. Enter https://github.com/ and create a Github account. For beginner, it could be hard to understand the home page of Github after you login. You may see unfamiliar tags on Github page. Ignore them and click `Start a project`

2. Fill out repository name like this `username.github.io`, you can change `username` to your own customize name. Then click `create repository`. In the future,  you can access your own website though the link like https://frankda.github.io


### Set up website locally with Jekyll

#### Install Git and Ruby

Examine whether you installed git and Ruby:
{% highlight ruby %}
# Look up git version you are using
git --version

# Look up ruby version you are using
ruby --version
{% endhighlight %}

If you haven't installed

install git by https://git-scm.com/

install ruby by https://rubyinstaller.org/downloads/, click `Ruby+Devkit xxx`

#### Install bundler

Print in command promt:
{% highlight ruby %}
gem install Jekyll bundler
{% endhighlight %}

#### Set up your local website

Continue printing in promt
{% highlight ruby %}
# Your website files will be set up to the target folder
cd user\anyfolder
jekyll new username.github.io
# Note your username should have the same name as Github project name
cd username.github.io
bundle exec jekyll serve
{% endhighlight %}

After finishing the steps above, open your browser and enter http://127.0.0.1:4000

Now you can see your website initial looking. Every time if you want to open your local website, enter `username.github.io` folder in commman promt and run `bundle exec jekyll serve`.

#### Deploy your website on Github Page

Using command promt enter `username.github.io` folder, for example: `cd user\anyfolder\username.github.io`. Then

{% highlight ruby %}
git init
git status
git add .
git commit -m "initial commit"
git remote add origin https://github.com/username/username.github.io.git
git push -u origin master
{% endhighlight %}

## Test your Github Page

Now you can use your browser and enter `https//username.github.io` to see your onw blog. There may be errors happened during this process because of any unknown bugs. Write down the error information and search to see how others solve these kinds of problems.

For beginner, you can use others' Jekyll theme to decorate your blog, I may also write a short article to illustrate how to change Jekyll theme and problems you may meet in changing theme.

# ALiAS Writes
*The official blog of ALiAS Community*

[![Build Status](https://travis-ci.com/asetalias/blog.svg?branch=master)](https://travis-ci.com/asetalias/blog)  [![HitCount](http://hits.dwyl.io/asetalias/blog.svg)](http://hits.dwyl.io/asetalias/blog) [![GitHub license](https://img.shields.io/github/license/asetalias/blog.svg?style=flat-square)](https://github.com/asetalias/blog/blob/master/LICENSE) 
![GitHub issues](https://img.shields.io/github/issues-raw/asetalias/blog.svg) ![GitHub repo size](https://img.shields.io/github/repo-size/asetalias/blog.svg)
![Twitter Follow](https://img.shields.io/twitter/follow/asetalias.svg?style=social)

This repository holds the source code and related content of the official blog for Amity Linux Assitance Sapience

ALiAS is a platform for upcoming developers for finding exposure by meeting the people working in related industries, learning various languages and becoming a better developer.

The website has been created using hugo and the theme used is hugo-massively-theme.

### WIP Branch for move to Jekyll Blog Theme

## Want to help out?
This website is currently under construction and all your inputs are highly appreciated.
-   Any writers willing to add your own thoughts to the blog can refer to the [instructions for Writer](https://github.com/asetalias/blog/#instruction-for-writers) section to learn about posting on the blog.
-   Any developers interested in the development of the blog and solving issues can refer to the [Instrucitons for Developers:](https://github.com/asetalias/blog/#instrucitons-for-developers) for help on how to contribute.
-   First time Git/Github users can refer to the [First time Contributors](https://github.com/asetalias/blog/#first-time-contributors) section for guides to help start contributing.

-   To be involved in the ongoing discussions please join our [Telegram Group](https://t.me/joinchat/KDFmCRdcpJrASFp5pKVaCA).

* * *

## Website Setup
<!--TODO: Need to be changed to Jekyll and Bundler instructions-->
0) For hugo installation and usage instructions, refer to [Hugo installation and setup](./INSTALLATION.md).
1) Clone this repository.
2) Open Terminal or your preferred CLI and navigate to the location of the repository.
3) Use the command `hugo server` to start a local sever of the website on your machine.

*The website will be available on <http://localhost:1313/>*

* * *

## Instrucitons for Developers:
<!--TODO: Need to be changed to Jekyll and Bundler instructions-->

`Git is required to contribute to the website and Hugo is required to run the site and test it on a local server.`

1) For hugo installation and usage instructions, refer to [Hugo installation and setup](./INSTALLATION.md).
2) Fork the repository and clone to your machine by using the command 
```
$ git clone https://github.com/<username>/blog
```
3) Make the changes locally and push them to your own repository.
4) Review the changes in your repository and submit a pull request.

*Hugo server starts a local server but hugo builds the website. Be careful when using the commands*

* * *

## Instruction for Writers:
<!--TODO: Need to be changed to Liquid Templating-->

The markup used for blog posts is **Markdown**

1) Fork the repository and clone to your machine by using the command 
```
$ git clone https://github.com/<username>/blog
```
2) Create you work file/blog post in `/content/post`, see existing files as an example.
2.5) The format needs to be exactly like [the sample post](./content/post/post.en.) for correct representation. 

Same has been given below. Edit and append this to the top of your post when finish writing. 

```
+++
title = 'WRITE_A_TITLE_DUH'
slug = 'give-a-descriptive-slug-like-this-please'
image = '/images/about.jpg'
date = "2012-02-06T00:00:00"
author = 'Creators of ALiAS Writes'
tags=['this', 'is', 'how', 'tags', 'looks-like']
categories =['Write', 'better-categries', 'than', 'this']
description = 'Small oneliners with a tinge of suspense works best'
disableComments = false
+++
```
 
3)  To run a local copy of the website, open the command prompt or your preferred CLI, change the directory to the address of the repository and use the command `hugo server` if you have hugo installed.
 For instruction on Hugo installation and use, refer to [Hugo installation and setup](./INSTALLATION.md).
4)  Submit a pull request to submit your work.

### Important Notes
<!--TODO: Need to be changed as per new Theming System details-->

-  Use `/blog/images/name_of_file` for your image source and keep the images in the images folder in static.
-  You can use `[img](../img.jpg#center)` to **center align** your images.
-  Make sure the format is **correct** as per **point 2.5**
-  Please don't add HD Images, 4K images to blog post. (size>=150KB)
-  All Content should be passed through Grammarly atleast once and spellchecked.

* * *

## First time contributors/Learn Git:

1) For a begineers guide on using Github, Visit [Hello World-Github](https://guides.github.com/activities/hello-world/).
2) For a guide to set up git for the first time, visit [Setting up Git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup).
3) For a begineers git guide, visit [git-a simple guide](http://rogerdudler.github.io/git-guide/).
4) For a detailed Git guide, you can read the book [pro git](https://git-scm.com/book/en/v2).

* * *

## Help and other Documentation:
<!--TODO: Need to be changed to Ruby & Jekyll-->

1) *For hugo documentation, [click here](https://gohugo.io/documentation).*
2) *For markdown cheat sheet, [click here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code).*
3) *For details about the theme, [click here](https://github.com/curtistimson/hugo-theme-massively).*
4) *Getting started with ALiAS: [Getting Started](https://bit.ly/2I833jJ)*
---
title: "Startup"
date: 2023-03-15T21:56:03+11:00
description: "A startup post to my blog."
tags: [Hugo]
categories: [Tutorial]
comments: false
draft: true
---

I have just recently created this blog, and I am testing out whether the post system works. I am unsure as to whether it will, but I hope it does. As to how I am making this blog, refer to below as I will explain exactly so. What to expect in this blog is a curious question, as I will do all the sorts. News, tutorials, how-tos, showcases, and generally me just doing a post on what I am doing at that moment in time. I might do something that has gone big on Stack overflow, a breach in a security company, etc, but you will have to wait and see as I am just setting up.

# How I made my website

This blog was made using [Hugo](https://gohugo.io/getting-started/) and it uses the m10c theme. If you have hugo, git & go installed, follow these steps to make a website similar to this one.

This tutorial is based on how you would do it on Windows, for any other OS refer to the [Hugo Quick Start guide.](https://gohugo.io/getting-started/)

```
$ hugo new site blog
$ cd blog
```
Initiates a hugo site, named blog, and enters its directory. You should see a folder named blog appear on your Desktop.

```
$ git clone https://github.com/vaga/hugo-theme-m10c.git themes/m10c
```
Imports our m10c theme into the themes folder, then into a new m10c folder.

Open the `config.toml` file in your preferred code/text editor, I use VSCode and Notepad++, but you may choose. Add `theme = "m10c"` to a new line in the configuration file and change the `title = ""` to whatever you wish. This will appear under your profile picture.

## Configuration

This is more complicated markdown stuff, so if you are having any troubles please read the more or less detailed [m10c theme tutorial](https://github.com/vaga/hugo-theme-m10c/) for better instructions.

In the `config.toml` file, you may define the variables as followed in the `params` section.:

- `author`: Name of the author
- `description`: Short description of the author 
- `avatar`: Path of file containing the author avatar image
- `menu_item_separator`: Separator between each menu item. HTML allowed (default: " - ")
- `favicon`: Absolute path of your favicon.ico file (default: "/favicon.ico")

### Theme Colour

In the `params` section, add the following lines of markdown and configure to your liking:
```
[params.style]
  darkestColor = "#d35050"
  darkColor = "#212121"
  lightColor = "#f5e3e0"
  lightestColor = "#f5f5f5"
  primaryColor = "#ffffff"
```

### Social Links

To add a social link, add these lines of markdown once again in the `params` section and configure to your liking.
```
[params.style]
  darkestColor = "#d35050"
  darkColor = "#212121"
  lightColor = "#f5e3e0"
  lightestColor = "#f5f5f5"
  primaryColor = "#ffffff"
```

### Menu Items

To add in a menu item, such as Tags, Categories, Home, etc, add the following lines of markdown in the `menu` section. Make sure to make a new page using `hugo new example/example.md` for something like an About page. The Tag and Category page is already made, so you do not need to make one.
```
[[menu.main]]
  identifier = "tags"
  name = "Tags"
  url = "/tags/"
```  

### Viewing the site

To view the site, start up the Hugo server using 
```
$ hugo server -D
```
-D is including all of our drafts, so make sure to define `draft: false` when making a new page so that you do not have to use `hugo server -D`, but just `hugo server`.

## Completion

If you did, thank you for reading this whole article, and I hope to make many more blog posts like this in the future, so I look forward to sharing my cyber journey with you.
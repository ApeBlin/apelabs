---
title: "Hosting Apelabs website using Hugo/Blowfish and GitHubPages"
description: "Hosting Apelabs website using Hugo/Blowfish and GitHubPages"
tags: ["new", "webDev"]
series: ["Website Documentation"]
date: "2024-08-26T00:00:00"
---
{{< lead >}}
My documented progress with all my oopsies and successes
{{< /lead >}}

## An Idea

I've had the idea of hosting my own project website, where I could showcase and manage my projects. I've been using Git for the software side, but I wanted something a bit more visible and easier to showcase if needed.
That's where this idea came along. Follow me on my journey of finding the right configurations and my thought process behind this project.

## Chooosing a framework

I had the idea of building the site myself using JS, React, and PHP. But for the sake of my sanity—and if I genuinely want this website to exist—I decided to use a framework. I went with Hugo due to having previous experience building small blogs and showcase websites for different cases.

While browsing for a good theme base for the site, I came across [Blowfish](https://blowfish.page/), and its configurability and features seemed like exactly what I needed, so I decided to use it.

## Blowfish setup

Blowfish uses the same setup as a normal Hugo project. There were a few options for installing this theme, but I decided to use the Git repo to build it myself. After setup, you get the basic example website, which is a lightweight version of the actual Blowfish site.

This proved to be extremely handy, as I could browse the example site, see features I liked, and easily view the configuration to understand how to build something like that myself.

It's relatively simple to write and build articles, heres an example of this exact article
```shell
---
title: "Hosting Apelabs website using Hugo/Blowfish and GitHubPages"
description: "Hosting Apelabs website using Hugo/Blowfish and GitHubPages"
tags: ["new", "webDev"]
series: ["Website Documentation"]

---
{{< lead >}}
My documented progress
with all my oopsies and successes
{{< /lead >}}

## An Idea

I've had the idea of hosting my own project website, 
where I could showcase and manage my projects. 
I've been using Git for the software side, but I wanted something a bit more visible and easier to showcase if needed.
That's where this idea came along. 
Follow me on my journey of finding the right configurations and my thought process behind this project. 
```
I edited the lines a bit to make it more presentable but in all it's simplicity this is how I'll be making content.

## Making the site mine

Now I had a beautiful website base with nothing on it. So, I started adding content. I knew I wanted my own tab for my projects. I thought about how I would categorize them. For now, I decided to have a main "Projects" page with all my projects, and from there, sub-pages for different categories: Electronics/Repair, Arduino, Software, etc.

## To-do

- Find a good workflow for writing articles.
- Create a gallery and add pictures. Evaluate if Hugo or Blowfish's own image compression will suffice.
- Host the website on GitHub Pages, and figure out how to work within the 1GB limit.


---

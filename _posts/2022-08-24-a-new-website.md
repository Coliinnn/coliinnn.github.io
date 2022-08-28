---
layout: post
title: "A new website"
author: "Colin Ganzevoort"
categories: blog
---

<p class="dropcap">Hello! If you're reading this, you probably found my new website. Although I've had my domain name for many years now, I really only used it for my custom e-mail. I did have a server running somewhere to display a very simple web page, but it contained no more than two words and a hyperlink to my LinkedIn profile.</p>

Since [I got a new homelab just months ago]({% post_url 2022-03-15-transforming-a-university-pc-to-my-new-homelab %}), I have entertained the thought of making a new website for myself, that could serve as an extension of my professional CV, but also as a personal blog. I have previously experimented with some blog writing, though I never did have a good platform to publish them. Before building the website, however, I had to decide for myself what kind of website I wanted and which tools would best suit my needs. There were several options that I could go with.

First, I considered going with [Wordpress](https://wordpress.org/){:target="_blank"}. [I have built a Wordpress website before for a client](https://dezeilmakerij.frl/){:target="_blank"}, and knew of its customisability with different themes and plugins. However, Wordpress seems to be quickly losing its charm, due to its [heavy use of resources and the status that it has gained as an outdated software that is frequently targeted by hackers](https://www.makeuseof.com/is-wordpress-still-worth-using/){:target="_blank"}. I am also not at very familiar with PHP and found it difficult to customise plugins and themes themselves in order to get the rather specific result that I was often looking for.

Then, I considered [Ghost](https://ghost.org/){:target="_blank"} as alternative, as I had heard much about it and it seemed a lot more modern, secure and fast than Wordpress. It is also a platform that is inherently dedicated to blogging and growing your audience. Getting Ghost up and running on my own server was however not as easy I had hoped. Immediately, the install process was finicky, and I did not like that I needed a separate Docker container for the (rather resource-heavy) MySQL database. With the limited resources that my homelab currently has, I need to make conscious decisions about the applications that I do and do not want to run.

<img src="/assets/images/Screenshot-ghost-db-resources.png" alt="Ghost resource usage" />
<figcaption>The Ghost database is one of the most resource-intensive containers on my system</figcaption>

Next, I found some information about [Static Site Generators](https://www.cloudflare.com/en-gb/learning/performance/static-site-generator/){:target="_blank"}. This was perfect and exactly what I was looking for. No databases, no comments; only super-fast performance, whilst still allowing for themes, plugins, and customisation, and still not requiring me to code each and every page individually. *The static site generator truly does feel like the best of both worlds.*

I ended up having to decide between two last options: Hugo and Jekyll. [Hugo](https://gohugo.io/){:target="_blank"} is the newer of the two, whereas [Jekyll](https://jekyllrb.com/){:target="_blank"} has existed since 2008 (that's 14 years!). Both offer themes and plugins, and they work in similar ways. The choice between these two did not seem to matter much, although Hugo is said to have a slightly steeper learning curve. I was initially looking to proceed with Hugo, as it is more modern and faster than Jekyll, but I found a beautiful theme that was only available for Jekyll.

---

And so, the current website is powered by Jekyll, combined with the [Hitchens theme](https://github.com/patdryburgh/hitchens){:target="_blank"} and hosted with [Github Pages](https://pages.github.com/){:target="_blank"}. I modified the theme heavily to my likings: I changed the colour scheme, I added an automatic dark mode, I added my own footer with social links, I customised the home page to contain the bulk of the information, added drop caps, and much more. It took upwards of a week to completely build the website, but I am very satisfied with the end product. *And the best thing is*: it's blazing fast, because it's all just static HTML and CSS. Without any databases and without hogging any resources on my personal server.
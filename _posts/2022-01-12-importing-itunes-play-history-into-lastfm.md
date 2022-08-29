---
layout: post
title: "Importing iTunes play history into Last.fm"
author: "Colin Ganzevoort"
categories: blog
---

##### Unfortunately, I am writing this post a few months after I actually went through this process. Although I do not remember all the details, I hope this information can still be of use to someone.

<p class="dropcap">Recently, I discovered <a href="https://www.last.fm" target="_blank">Last.fm</a>. Last.fm is a website that provides track, album and artist recommendations based on listening history. Of most interest to me is that Last.FM also provides detailed statistics of users' listening history, such as play counts and which artists and albums I have listened to the most.</p>

Although iTunes also keeps track of play counts, it is limited to individual track counts and iTunes provides no way of visualising the data. And so, I went looking for a solution to import my listening history (of six years!) from iTunes into Last.FM.

In the end, I ended up using [Universal Scrobbler](https://universalscrobbler.com/){:target="_blank"}. I exported all of my iTunes statistics by selecting the columns that I wanted and then hitting CMD+A and CMD+C to copy the rows of information. This I could simply paste into a CSV spreadsheet file. These spreadsheets I had to slightly adjust and split into multiples, as even the Premium status did not allow me to upload all of my sixty-thousand scrobbles at once. This is actually a Last.fm API limitation, but nevertheless I had to stagger my uploads over the course of a month, as I could upload around 2000 scrobbles per day.

---
layout: post
title: "Transforming a university PC to my new homelab"
author: "Colin Ganzevoort"
categories: blog
---

> A 'homelab' is "the name given to a server (or multiple server setup) that resides locally in your home and where you host several applications and virtualized systems for testing and developing or for home and functional usage." — [What is a Homelab and Why Should You Have One?](https://linuxhandbook.com/homelab/){:target="_blank"}

<p class="dropcap">A few days ago, I was walking around with some of my peers in the library section of <a href="https://www.rug.nl/gmw/" target="_blank">my faculty at the University of Groningen</a>. As I descended down the stairs and entered the hallway, I noticed a large table containing a bunch of monitors, keyboards, mice, and even University computers. There hung a sign, indicating that the IT department would no longer be using these units and that students were free take any of the items and bring them home.</p>

The people that I was with were mostly interested in the monitors. Of course; normally, I would have been, too. However, just a few months ago I started tinkering with a Raspberry Pi 4 and I found myself increasingly often browsing the [homelab](https://www.reddit.com/r/homelab/){:target="_blank"} and [self-hosted](https://www.reddit.com/r/selfhosted/){:target="_blank"} subreddits. The people on these subreddits often show off systems that are not even remotely comparable to a Raspberry Pi, but the Raspberry nevertheless offers a respectable way to start experimenting with Linux, Docker, programming, systems administration, and networking.

> citation ""
> "The Raspberry Pi offers a respectable way to start experimenting with Linux, Docker, programming, systems administration, and networking."


However, I soon ran into the the limits of the Raspberry Pi, mostly as a result of the ARM chip and the 2GB of RAM that mine was equipped with. Within the homelab communities, I had often seen people recommend Small Form Factor computers because they are relatively small, whilst the x86 CPU offers a whole lot more power than an ARM chip. And so I started looking online for these SFF computers. The search did not last long, for I found myself in that very hallway in the library of my faculty; no two weeks after starting to look for a new computer.

---

Indeed, those units in the library were exactly what I was looking for. It is an HP Compaq Pro 6300, with the Small Form Factor. The computer originally had (an impressive) 8GB of RAM installed and a 256GB SSD, which I upgraded to 16GB of RAM and two 256GB SSDs. It has a core i3-3220 (Ivy Bridge) CPU @ 3.30GHz, with 2 cores and 4 threads. Although this is certainly not the newest generation, the i3-3220 is still an immense upgrade from the Raspberry Pi.

<img src="/assets/images/IMG_1424.jpeg" alt="The computer">
<figcaption>The computer that I got from the university. It even has the little red IT plate on it still.</figcaption>

On the Raspberry, I ran just a handful of services that I threw together in a single [docker-compose](https://docs.docker.com/compose/){:target="_blank"} file. But now, I decided to take a different approach. After thoroughly cleaning the case inside and out, I installed [Proxmox](https://www.proxmox.com/en/){:target="_blank"} as host OS on the system. This allowed me to create several virtual machines to group my services together. Moreover, I could use this as an opportunity to learn about virtualisation software and to work more intricately with Linux.

<img src="/assets/images/IMG_9704.jpeg" alt="The computer">
<figcaption>Installing the Proxmox hypervisor on the system</figcaption>

<br>
<div class="divided"></div>
<br>

**Update.** Now, on August 27th, 2022, my homelab has been running nicely for nearly five months. Although I did encounter numerous issues that needed fixing, and the server was often down for extended periods of time, the server has now come to a place where it can safely run for long periods without any required intervention. At the time of writing this, the server runs six virtual machines and 41 Docker containers; each containing a different service or database.

That one afternoon in the library has surely resulted in a lot of long days, late nights, and much time spent thinking about issues and solutions. But now, five months later, I have learned so much: about hardware and general Linux usage, about virtualisation, containerisation and Docker; about networking and network-attached storage (NAS); and about automation tools to manage all of the virtual machines at once.

Yet, as with anything, a lot remains to learn. I look forward to the challenges that will surely arise and the solutions that I can think of to get past those challenges. I look forward to deepening my Linux knowledge further and to gain more experience with the management of such systems.

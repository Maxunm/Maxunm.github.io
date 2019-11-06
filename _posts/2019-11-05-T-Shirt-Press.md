---
layout: post
title: "T-Shirt Press"
date: 2019-11-05
excerpt_separator: "<!--more-->"
---
## T-Shirt Press
The goal of this project is to make a working T-Shirt press in the style of the Cricut [Easy Press](https://cricut.com/en_us/cricut-easypress).
The project is still in it's early days but I will keep this post up-to date with the current status.

The idea came for this project when using a vinyl cutting machine. Thinking of how it would be nice to be able to
make T-Shirts with with it.
<!--more-->
##### Heated Bed
The real first step of this project was to choose an appropriate heated bed to build the press from. I searched for quite some time to find one that would be economical and still perform adequately. I explored options like getting a silicone heating mat custom made, and then affixing it to a plate of my own creation. I found this would be more work and more expensive than it might be worth in customizability. I overall ended going with a [e3d High Temperature Heated Bed](https://e3d-online.com/high-temperature-heated-beds) I went this route because it had all the features that I needed, a high max temp (200&deg;C) and a quick heat-up time (80 seconds to 100&deg;C), and it was fairly economical too (INC. VAT &pound;132). This heated bed also included a resistive `104-GT2 "E3D"` thermistor, so I would not have to pick one of my own.

##### Control systems
The next step after picking a heated bed I needed to select an appropriate microcontroller to control everything. I am currently using a STM32F429I-DISC1 because I have used it extensively in one of my courses in university. I will use this with other electronics to monitor the temperature of the hot plate and control it using a solid state relay. The following equation will be used to determine the actual temperature of the hot plate$$ \frac{1}{T} = \frac{1}{T_{0}} + \frac{1}{\beta} + \ln{\frac{R}{R_{0}}} $$[...](https://community.st.com/s/question/0D50X0000AU39YK/is-stm32-microcontrols-are-capable-to-calculate-natural-logarithm-)

[//]: # (This loads the latex converter.)
<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
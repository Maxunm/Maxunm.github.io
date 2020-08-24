---
layout: post
title: "Fax Machine"
date: 2020-8-20
excerpt_separator: "<!--more-->"
---
## Turning my printer into a fax machine  
This is a quick post today. Two days ago, I bought a brand-new Brother DCP-L2550DW and I had the grand idea to turn it into effectively a fax machine. To do this I will have a webpage hosted that accepts uploads of pdf files. These pdf files are then immediately printed and then deleted. This involved a couple of fairly simple things that came together to make this all work.  
<!--more-->  
  
### The webpage  
The webpage is just a simple page that displays an upload box and accepts uploads. The most difficult part of this was to get the drag and drop functionality of the upload box to work correctly. Mostly the webpage was written/programmed by [Dave Stewart](https://gitlab.sfnetwork.us/public). He did this using a javascript library for the drag and drop feature called dropzone.js. The rest of the website is done in php, and does the complete upload to the server and then calls my script.  
  
### Server side  
So, the server is set up using apache2 which hosts the page written by Dave. After a file is uploaded the last thing the php script does is call my bash script. My bash script gets the file name to print, prints it and promptly deletes the file.  
  
### CUPS  
One of the most confusing parts of the server-side configuration is setting up cups to manage my printer more easily than trying to manually set all of the settings. Brother also has a driver available for Linux, which my server is running, and using this It automatically configured all of the settings for the printer. The one setting that I did have to change was the paper size which is A4 by default.  
  
### Conclusion  
This was just a fun little project with my new printer and hopefully someone doesn't use all my paper.

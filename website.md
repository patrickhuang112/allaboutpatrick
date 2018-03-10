---
layout: page
title: Creating this website
---

<b>Step 1</b>: What I first did was visit the jekyll website and go to this page about jekyll on windows 10.

<a href = "https://jekyllrb.com/docs/windows/">Jekyll on windows</a> 

I followed the instructions on the website and eventually had everything ready for website creation

<b>Step 2</b>: I searched online for jekyll themes. The theme I settled on was called lanyon, a very simplistic theme that would allow me to quickly launch my website. 

<a href = "http://lanyon.getpoole.com/">Website showcasing the lanyon theme</a>

I then headed over to their github repository and forked their code to my account. After forking, I cloned the files to my local computer, to a folder called "allaboutpatrick".
"git clone 'link from github' "

<b>Step 3</b>: Editing pages and content was quite easily. Each content file was in markdown so modifying content was very simple. Once I had finished modifying my content, I uploaded my changes to my own repository on GitHub to keep an online revision control.


"git status" : I used this command to view what content was to be pushed online.

"git add "file name" : I used this command to add revized local files to be pushed online.

"git commit -am "comment" : I used this command to add a comment detailing what was changed in the local file.

"git push" : I used this command to push comments and local files online.

<b>Step 4</b>: Setting up Amazon Web services. My father and I worked to buy a domain and to set up the address for the website. This step of the creation process will be updated later.

<b>Step 5</b>: The contents of my website were stored in the Amazon S3 bucket. To push local changes to the actual website on the world wide web, a series of commands were executed.

First, I navigated to my "_site" folder locally. From there, I ran bash and ran this command.

"aws s3 sync . s3://patrickhuang.me"

This command essentially synchronizes the local files with the files in the S3 bucket, essentially updating the public website.


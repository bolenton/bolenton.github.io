---
layout: post
title: Hosting & custom domain on Github Pages
Date: 2015-04-17
categories: Guide, Beginner, Tutorial
comments: true
banner_image: "/assets/img/header/sample-image-1.jpg"
featured: true
---

Did you know that Github will allow anyone to host their static webpages for free? Yes I'm serious! It's very easy to set up. The best part is ... You can use your own custom domain!
Don't believe me? What if I told you that this blog that you're reading right now is being hosted free of charge on Github Pages? Here's my github: [Look for yourself](https://github.com/bolenton/bolenton.github.io).
Believe me now? Good! If you want to set up your own webpage with your custom domain and host it for free than keep reading.
<!--more-->

## <i class="fa fa-arrows-h"></i>Step 1: Create your webpage
If you already have a website, than you can move on to step 2, if not than today is good day to start. I suggest starting a blog. A blog is a great way to establish a more meaning presence online. You can leverage it to build your own [personal online brand.](http://www.forbes.com/sites/shamahyder/2014/08/18/7-things-you-can-do-to-build-an-awesome-personal-brand/) Don't know where to start? I got you covered. John Sommez of [Simpleprogrammer.com](http://simpleprogrammer.com/?__s=e9nxoo3daippuegoyzyj&utm_campaign=lesson-5-do-you-know-how-to-get-traffic-for-your-blog&utm_medium=email&utm_source=how-to-create-a-blog-that-boosts-your-career-course) has an excellent email course called: [How To Build A Blog That Will Boost Your Career](http://t.dripemail2.net/c/eyJhY2NvdW50X2lkIjoiOTUyNDk2NiIsImRlbGl2ZXJ5X2lkIjoiMjQ3MzM4MTciLCJ1cmwiOiJodHRwOi8vZGV2Y2FyZWVyYm9vc3QuY29tL2Jsb2ctY291cnNlLz9fX3M9ZTlueG9vM2RhaXBwdWVnb3l6eWpcdTAwMjZ1dG1fY2FtcGFpZ249bGVzc29uLTUtZG8teW91LWtub3ctaG93LXRvLWdldC10cmFmZmljLWZvci15b3VyLWJsb2dcdTAwMjZ1dG1fbWVkaXVtPWVtYWlsXHUwMDI2dXRtX3NvdXJjZT1ob3ctdG8tY3JlYXRlLWEtYmxvZy10aGF0LWJvb3N0cy15b3VyLWNhcmVlci1jb3Vyc2UifQ). It's a great course that walks you through the process. You can expect a review of that course soon. 

So you decided to start a blog. Now what? There are many way you could go. Like Wordpress, Tumblr, or even Blogger. But that would defeat the purpose of this article. We want to use Github Pages to host a static page for free. So I recommend using a static blog generator. I personally use [Jekyll](http://jekyllrb.com/) for this blog. Buts there are many out there. He's a list of some of the more popular ones. [Static Blog Generators](http://www.sitepoint.com/6-static-blog-generators-arent-jekyll/). Choose one, read the instructions, and get your blog set up!

## <i class="fa fa-expand"></i>Step 2: Add your site to Git Version Control
Great you made it to step 2. Now that your blog is ready, let's put it under version control using [Git](http://git-scm.com/). This Article assumes you have [Git installed](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git), you have a github account and can [push to it](http://guides.railsgirls.com/github/). 

* This step is very important: create a simple .txt file and name it `"CNAME".` Open the file and type your custom domain name in it. Save it.
{% include image_caption.html imageurl="/assets/img/post_img/cname.png" title="CNAME" description="Create a simple .txt file and name it CNAME" %}

1. Ok crank up your terminal, and cd into the directory that your site lives in.
2. Head back to your terminal. Its time to initialize version control by entering the command. `$ git init`
3. Now enter type `$ git add .`  to add the entire project under git tracking.
4. Let's commit it: `$ git commit -m "first commit"`
Wonderful your site is ready and under version control. Now the fun begins. 

##<i class="fa fa-cog"></i>Step 3: Push to Github
We are finally ready to push to github and see our site automatically running live online for free!

1. Launch [github.com](https://github.com/) and sign in.
2. On your home page click the big green button that says "+ New repository."
3. For your page to automatically be hosted there is a naming convention you must follow. Name your new username.github.io leave everything else as is and press "Create Repository. 


    {% include image_caption.html imageurl="/assets/img/post_img/github.png" title="CNAME" description="Name your repository, don't do anything else, hit 'Create Repository'" %}


Now follow the instruction to push your blog to your new repository.
That's it! Your new page should be up at www.username.github.io
If you don't see it right away, give it a few minutes, ten at the most.

##<i class="fa fa-spinner"></i>Step 4: Assign your custom domain to you new github page
This will vary depending who your domain is registered with. I have GoDaddy so the images are specific to that. But the steps should be similar with other domain providers. Here is how I did it.

1. I signed into my GoDaddy account and selected "manage  domains" (I have 3 domains). I selected the domain I wanted to use clicked "Manage Connection". 
2. On the "Domain Details" page I clicked the "DNS ZONE FILE" tab. 
3. Edit "A-Host" and point it to 192.30.252.153
4. Now edit the www potion of "CName (Alias)" and point it to username.github.io. Make sure to save everything. 
Once you save this could take up to an hour to update completely. Now your "customdomain.com" should point to username.github.io, however what if the the user enters "www.customdomain.com"? Let's fix it so that will point to username.github.io as well. 
1. Again I select my domain and press "Manage Connection", this time on the "Domain details" page I select the "Settings" tab.
2. Under Forwarding -> Domain, I click "manage". Click on "Update Forwarding". 
3. In "Forward to:" type www.customdomain.com
4. Make sure 301 (Permanent) is selected. Save your work.
That's it. Allow it about 1 hour for everything to update. 

Let me be the first to congratulate you. You have a website up and running, under version control, with your own domain name and hosted free of charge!
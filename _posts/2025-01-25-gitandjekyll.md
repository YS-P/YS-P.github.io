---
layout: post
title:  "Creating a Blog with Jekyll"
author: 2han
featured: true
categories: [ Jekyll, github ]
image: assets/images/post1.jpg
rating: 3
---

I decided to document the initial setup process of creating this blog with Jekyll. It seems like I spent quite long time for focusing on details like design, but if you don't get unnecessarily caught up in such things like I did, it actually seems quite simple.


## Jekyll
<div style="text-align: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/jekyll_image.png" alt="walking" style="width: 50%; max-width: 300px;">
</div>
"Transform your plain text into static websites and blogs." This is Jekyll's official tagline. As the phrase suggests, it's a highly useful tool for creating static websites. It’s especially convenient to use because of its excellent integration with GitHub.


## Select the Theme
This is the most important part, in my opinion 🤣  
You can find several websites on Google, so you can simply fork a theme from their repository.

<div style="text-align: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/git_screenshot.png" alt="walking">
</div>

I chose a theme called "Mediumish." It's simple and modern.

<div style="text-align: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/gitname.png" alt="walking">
</div>

Now, we should change the Git repository name to '{youraccountname}.github.io.'  
Congratulations, you now officially have your blog! Simple, right?

You can find your deployment link in your GitHub repository under:  
'Settings > Pages.'
<div style="text-align: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/gitlink.png" alt="walking">
</div>


## Error Handling
The only error I faced during the process was with image loading.  
When I ran my blog on 'localhost:4000', it worked perfectly. However, with the deployment link, the images didn’t load.  
The solution was simple: just clear your browser’s cache, and you’ll find a perfectly functioning website.


## Some YouTube videos you may find helpful
Actually, I didn’t watch this video all the way through, haha... but it seems helpful. 
At least I watched the first few minutes.

<p><iframe width="700" height="350" src="https://www.youtube.com/embed/g6AJ9qPPoyc?si=yjq7KFqDi8m_mnf5" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></p>
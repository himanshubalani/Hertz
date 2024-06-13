---
title: "How I made my portfolio website in Flutter"
datePublished: Thu Jun 13 2024 07:28:43 GMT+0000 (Coordinated Universal Time)
cuid: clxcxuuoo00070aju46wh3rjj
slug: portfoliowebsiteinflutter
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1718175455719/b49e1cf4-aa74-4db9-874e-f871fc8128a2.png
tags: design, web-development, flutter, ui, portfolio

---

As we all know, all developers should build a portfolio website once in their journey. I realized that as well and started building one in 2022. It's a canon event.

![It's a canon event.](https://www.looper.com/img/gallery/spider-man-across-the-spider-verse-has-massive-implications-for-loki-season-2/l-intro-1685738344.jpg align="left")

I used one of those free HTML website templates you find at HTML5 UP and deployed it in Github Pages in 2-3 days. It looked like this-

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1718261882960/e4b219bf-bfad-4093-96ad-f9d85e0dcddc.png align="center")

But more than a year passes, and I release that my portfolio website didn't stand out as much as I wanted it to be. So I decide to build it again from scratch.

### A design that spoke to me

I went and watched several YouTube videos on making portfolio websites for getting design inspiration. All of them were either very minimalistic or very extravagant. Nothing in between. So I thought let's start with a template to get a fair idea of the webaites' contents. Astro seemed like a fair choice for that. Many templates were looking good but [Brutal](https://brutal.elian.codes/) seemed like a odd choice. In all the minimalistic templates I saw, it stood out.

**Literal Color Vomit.**

I researched more about Brutal style and came across Neobrutalism. A concept very new to me! I used several colors as backdrop for my pages. Next, I turned my attention to the top bar. Given the riot of colors in the main content, I knew it needed to be more subdued. Drawing inspiration from the Astro template, as well as platforms like Gumroad and Figma, I designed a top bar that balanced the color of the rest of the site. I designed a favicon too!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1718035657211/c6e24354-ad59-4546-a055-042cd4c10880.jpeg align="center")

I wanted to build a personal brand so I made efforts to make similar banners for my social accounts so that they match the website and make it a cohesive experience for anyone trying to get to know me. Take my Twitter(X) / Linkedin Banner below for example. Or the blog post cover image above.  

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1718262917183/1504569d-bbae-40f1-b50d-4f2649153bef.png align="center")

### Choosing a tech stack

I could very well have used HTML and CSS, maybe use Tailwind, then add some JS in the mix to make the website. But I thought why not give Flutter a chance. I am already comfortable with Flutter an this could further help my skills.

<div data-node-type="callout">
<div data-node-type="callout-emoji">❗</div>
<div data-node-type="callout-text"><strong>Do not use Flutter Web for building Websites.</strong> It's intended for <strong>WebApps</strong> that allow for more functionality. I ignored this. You probably should not.</div>
</div>

### Building the portfolio

I used the command `flutter create portfolio --platforms web` for creating the project. The process is exactly the same as coding an app since it's Flutter. I made a custom appbar, custom buttons and several custom widgets. Designing a responsive website that accommodates various screen sizes was essential. The site features both desktop and mobile versions that seamlessly switch based on the device's screen width. I used `screenutil` package to dynamically change sizes of widgets and text.  
  
Once I was done, it was time to build the webapp. The release build is generated using a single command `flutter build web --release`  
A release build uses [dart2js](https://dart.dev/tools/dart2js) (instead of the development compiler used in debug mode) to produce a single JavaScript file `main.dart.js`. The index.html file in your Flutter build uses main.dart.js file to load the entire WebApp. Flutter lets us choose a renderer for the web. There are 3 options-

* HTML Renderer
    
* Canvaskit
    
* Web Assembly or Wasm (new)
    

I used Canvaskit for my project. I intend to shift to Wasm once it is available on iOS and FireFox.

### Deployment

I used **GitHub Pages** to deploy my portfolio website as it is very easy and reliable. I just need to push the build files to the [repository](https://github.com/himanshubalani/himanshubalani.github.io) and a deployment is made.  
I always wanted my own domain. So after thinking about it, I bought my first domain name, [himanshubalani.com](https://himanshubalani.com) and added the DNS record for GitHub Pages so thst my website can use the custom domain.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1718262523182/7bf3561f-ca84-46a6-b60d-359d30e54ed6.png align="center")

<div data-node-type="callout">
<div data-node-type="callout-emoji">😅</div>
<div data-node-type="callout-text">That's three "himanshubalani" mentions in a small part of the screen. There are five on the homepage! It might be excessive, but sometimes you have to do what you have to do. Haha!</div>
</div>

### A Challenge

One of the challenges I faced was optimizing the initial load time. Flutter web apps can be hefty, so I had to employ various optimization techniques to ensure the site loaded quickly and ran smoothly. This included lazy loading images, minimizing the use of heavy animations, using widgets wisely, ensuring efficient state management and editing the load script to run and parse in parallel so that Page Loading times are improved.

You can read more about how I improved my portfolio's performance in my previous blog post below-

%[https://hashnode.com/post/cltrbxwfh000309l2byig85x0] 

### Future Enhancements

Looking ahead, I plan to add a Headless CMS by Hashnode to my blog. This will allow me to design the look and feel of the blog more freely and integrate it seamlessly into my website. Currently, I have a custom domain, [`blog.himanshubalani.com`](http://blog.himanshubalani.com) but I believe using Hashnode's Headless CMS, I can design the webpages to my liking.

### Closing

Building your own portfolio website from scratch is a great experience, and I believe all developers should create one at least once in their careers. It’s an opportunity to showcase your skills, creativity, and build a personal brand in a unique way.

You can visit my portfolio website at [himanshubalani.com](http://himanshubalani.com).

Let me know if you liked my website, and feel free to drop any suggestions in the comments. Your feedback is highly appreciated and will help me improve my site even further. Thank you for taking the time to explore my work!
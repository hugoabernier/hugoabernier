---
title: "Ultimate Developer Tool List for SPFx"
aliases: 
  - 2019/03/14/ultimate-developer-tool-list-for-spfx
  - /2019/03/14/ultimate-developer-tool-list-for-spfx
date: 2019-10-29T10:07:47+06:00
draft: false

# post thumb
image: "posts/ultimate-developer-tool-list-for-spfx/brushes-3129361.jpg"

# meta description
description: "I asked the SharePoint Developer Community what development tools they use on their workstations to develop SPFx solutions. They came through!"
summary: "I asked the SharePoint Developer Community what development tools they use on their workstations to develop SPFx solutions. They came through!"

# taxonomies
categories:
  - "SPFx"
tags:
  - "React"
  - "SPFx"

# post type
featured: true
author: "Hugo Bernier"
---

## Introduction

[Scott Hanselman](https://www.hanselman.com/) is someone that I admire, both as a Developer and as a Human Being. I never miss a chance to attend his presentations. I’m not smart enough to understand everything he talks about all the time, but he’s always entertaining to watch.

Everyone once in a while, he creates an [ultimate list of developer and power tools](https://hanselman.com/tools) which always has one or two new tools I didn’t know about. Any serious developer should look at his list as a great starting point to configure their workstation.

When [SPFx first came out](https://github.com/SharePoint/sp-dev-docs/wiki/Drop-1), I had never touched Node.js, React, or TypeScript. Visual Studio Code was (in my mind) just a free/lightweight version of Visual Studio — why would anyone use VS Code over the full-on Visual Studio?!

And don’t get me started about GitHub!

I had a steep learning curve ahead of me. And I had a whole new set of development tools to install on my workstation. It took me a while to figure out what I needed to install to be efficient at creating SPFx solution.

I’m in the process of updating my Windows 10 workstation and, as I was writing down the list of things to re-install, I thought I’d share my list. This list is specifically for people who want to write SPFx solutions on Windows. It isn’t as comprehensive as Scott’s list, but I hope that it will help anyone getting started with SPFx development.

I also work with .NET, Azure, VR and AR, and Dynamics 365, so I have other tools on my workstation, but I wanted to focus on SPFx development.

If you develop SPFx solutions and see that I forgot anything here, I would love to hear from you!

> **NOTE:** I’m a bit of a minimalist when it comes to installing stuff on my workstation. I hate installing things that will automatically start when I launch windows (that’s why I never install anything from Adobe anymore). You’ll rarely find anything in this article that will completely change how your operating system works or takes over your machine… and if you do, it is because I feel that the trade-off is worth it.

## Mandatory

### Node.JS

[Find the **.MSI** file](https://nodejs.org/dist/latest-v10.x/) in the list that suits your workstation (x86 or x64). As tempting as it may be to download the latest version, **don’t**. The only version that is officially supported for SPFx development is **10.x**.

### Gulp

[Gulp](https://gulpjs.com/) is a tool that helps automate building your solutions. Once NodeJS is installed, install **Gulp** by launching the **Node.js command prompt** and type the following:

    npm install -g gulp

### Yeoman

[Yeoman](http://yeoman.io/) is a tool that scaffolds solutions. Think of it as the Visual Studio new project wizard, if the new project wizard was command-line driven, open-sourced, and contained a bazillion project types. To install it, use your **Node.js command prompt** and type:

    npm install -g yo

### SharePoint Framework Yeoman Generator

Now that Yeoman is installed, you need to add what is essentially your "_SPFx Project Wizard_". To do so, use your **Node.js command prompt** and type:

    npm install -g @microsoft/generator-sharepoint

## Recommended


### [Visual Studio Code](https://code.visualstudio.com/)

When I first started writing SPFx solutions, I refused to use Visual Studio Code (real developers use Visual Studio, right?). Unfortunately, Visual Studio messed up my SPFx solutions more than once and I quickly learned to appreciate Visual Studio Code. Visual Studio no longer messes with your SPFx solutions, but I still use VS Code for all-things-SharePoint.

### [Git for Windows](https://git-scm.com/downloads)

Even if your company uses Azure DevOps or TFS for source control, you should install Git to make your life easier when downloading [SPFx code samples](https://github.com/SharePoint/sp-dev-fx-webparts).

### [Cmder for Windows](https://cmder.net/)

If you’ve ever wondered what that cool command-line they use on the SharePoint Development Community calls, you have found it! Follow [my instructions](https://hugoabernier.github.io//2018/05/27/changing-your-command-prompt-to-display-node-module-and-git-information-like-the-sharepoint-conference-presenters/) if you need help installing it. ![Cmder](../../images/post/uploads/2018/05/cmder-sample-2.webp)

### [Fira Code Font](https://github.com/tonsky/FiraCode)

This font will add the cool visualization to the Cmder command prompt. You should also [configure it as your default Visual Studio Code font](https://hugoabernier.github.io//2019/03/16/setting-fira-code-as-your-default-visual-studio-code-font/) ![Fira Code Font](https://camo.githubusercontent.com/3a8948f34284f378ead7af5846aa432035c687ad/687474703a2f2f732e746f6e736b792e6d652f696d67732f666972615f636f64655f6c6f676f2e737667)

### [Cmder Powerline](https://github.com/AmrEldib/cmder-powerline-prompt)

When paired with the Fira Code font (above), it will add that cool command-prompt to Cmder.

### [Postman](https://www.getpostman.com/downloads/)

Test your APIs using this awesome tool. It can even intercept calls and replay them. I use this tool all the time when I’m trying to understand how SharePoint does something.

### [Fiddler](https://www.telerik.com/fiddler)

Use Fiddler to capture your workstation’s network traffic and diagnose issues. For example, if you want to know how the Microsoft Teams app retrieves your list of groups, use Fiddler to capture what calls it makes.

### [CLI for Microsoft 365 CLI](https://pnp.github.io/cli-microsoft365/)

A command-line interface that lets you do tons of stuff in Office 365 and SPFx solutions. To install, use your **Node.js command prompt** and type the following:

    npm i -g @pnp/cli-microsoft365

### [PnP PowerShell](https://github.com/pnp/pnp-powershell)

An awesome library of PowerShell commands that allows you to perform complex provisioning and artifact management actions towards SharePoint. Uses a combination of CSOM and REST behind the scenes, and works against both SharePoint Online as SharePoint On-Premises.

### [SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251)

Use it to create SharePoint Online sites and add users, you can quickly and repeatedly perform tasks much faster than you can in the Office 356 admin center. You can also perform tasks that are not possible to perform in the Office 356 admin center.

### [PnP Yeoman Generator](https://pnp.github.io/generator-spfx/)

If you find yourself always adding the PnP developer controls, PnP Property Controls, PnPJs, unit testing, etc. to your SPFx solutions, you should probably try the PnP Yeoman Generator. It is **built on top** of the SPFx Yeoman generator, so you’re not missing out on anything the SPFx generator will give you, but it automatically adds many other useful features — like unit testing, code linting, bundle optimization. To install it, use your **Node.js command prompt** and type:

    npm install -g @pnp/generator-spfx

## Visual Studio Code Extensions

### [GitHub Pull Requests](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)

Allows you to review and manage GitHub pull requests in Visual Studio Code. ![GitHub Pull Request](../../images/post/uploads/2019/03/image-1594305412847.png)

### [Paste JSON as Code](https://marketplace.visualstudio.com/items?itemName=quicktype.quicktype)

Convert JSON object to typescript interfaces as you paste into Visual Studio Code. What, you thought I typed all those classes? ![Past JSON as Code](https://raw.githubusercontent.com/quicktype/quicktype-vscode/master/media/demo-interactive.gif)

### [Rencore Deploy SPFx Package](https://marketplace.visualstudio.com/items?itemName=RencoreGmbH.vscode-spfx-deploy-package)

Easily deploy a SharePoint Framework solution package to SharePoint Online directly from Visual Studio Code. 

![Rencore Deploy SPFx Package](https://github.com/rencoreab/vscode-spfx-deploy-package/raw/master/./assets/deploy-sppkg-in-app-catalog.png)

### [Rencore SPFx Script Check](https://marketplace.visualstudio.com/items?itemName=RencoreGmbH.vscode-spfx-script-check)

Using the Rencore Script Check Visual Studio Code extension you can easily reference external libraries in SharePoint Framework projects the right way. Additionally, you can ensure, that the CDN they are using is well performing. 

![Rencore SPFx Script Check](https://raw.githubusercontent.com/rencoreab/vscode-spfx-script-checker/master/assets/script-global.gif)

### [Rencore Tenant-Wide SPFx Extension Deployment](https://marketplace.visualstudio.com/items?itemName=RencoreGmbH.rencore-tenant-wide-spfx-extension-deployment)

Easily add tenant-wide deployment information for your SPFx extension directly from Visual Studio Code. 

![Rencore Tenant-Wide SPFx Extension Deployment](https://raw.githubusercontent.com/rencoreab/vscode-spfx-tenant-wide-extension/master/assets/tenant-wide-deployment-menu.png)

### [SPFx Debug Configuration](https://marketplace.visualstudio.com/items?itemName=eliostruyf.spfx-debug)

This Visual Studio Code extension can be used to add the required configuration for debugging your SharePoint Framework.
### [SPFx Essentials](https://marketplace.visualstudio.com/items?itemName=eliostruyf.spfx-essentials)

This is an extension pack that contains useful extension for SharePoint Framework projects. Most of the extensions I listed here are already included in Elio’s awesome list.
### [SPFx Localization](https://marketplace.visualstudio.com/items?itemName=eliostruyf.vscode-spfx-localization)

This extension for Visual Studio Code makes it easier to work with locale resource files in SharePoint Framework projects. The extension has the ability to export all locale labels to a CSV file to make translations easier to process. With this extension, **you have absolutely no excuse to hard-code your text in English within your solutions**. ![SPFx Localization](https://github.com/estruyf/vscode-spfx-localization/raw/master/assets/localization-csv-export.gif)
### [SPFx Snippet](https://marketplace.visualstudio.com/items?itemName=eliostruyf.spfx-snippets)

I never realized how much I use this extension until I tried to write `spfx-rcc` for a web part on a machine that didn’t have the extension installed. Take it from the _World’s Laziest Developer_, you **need** this extension. ![SPFx Snippet](https://github.com/estruyf/vscode-spfx-snippets/raw/master/assets/spfx-snippet-demo.gif)
### [SPFx Task Runner](https://marketplace.visualstudio.com/items?itemName=eliostruyf.vscode-spfx-task-runner)

This extension allows you to easily run SharePoint Framework tasks with a couple of mouse clicks. At the moment you can for example list all the available gulp tasks in your project, start the local development server and create debug or release solution packages or pick a task to run from the list of available tasks. ![SPFx Task Runner](https://github.com/estruyf/vscode-spfx-task-runner/raw/master/assets/contextmenu-actions.png)
### [SP Formatter](https://marketplace.visualstudio.com/items?itemName=s-kainet.sp-formatter)

Sergei strikes again with a great extension that works with the [SP Formatter](https://github.com/pnp/sp-formatter) browser extension to make it easy to use syntax highlighting on list formatting.
### [SharePoint Typed Item](https://marketplace.visualstudio.com/items?itemName=s-kainet.sharepoint-typed-item)

Sergei’s awesome extension generates interfaces based on list and content type fields. Also check out Sergei’s [SPFx Rest Client](https://marketplace.visualstudio.com/items?itemName=s-kainet.rest-client) ![SharePoint Typed Item](https://raw.githubusercontent.com/s-KaiNet/vscode-sp-typed-item/master/assets/sp-typed-item.gif)
### [Prettier — Code Formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

This extension format your JavaScript / TypeScript / CSS using Prettier.
### [SPGo for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=SiteGo.spgo)

SPGo allows you to develop SharePoint web solutions from your local PC using Visual Studio Code. It pulls down remote folders from SharePoint to your local workspace and automatically publishes files when you save. It is one of those "where has this been all my (SharePoint) life?!" extensions.
### [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)

If you maintain any kind of Markdown documentation, or if you contribute to Microsoft Docs (you should!), you should install this extension pack that will make your life much easier. Thanks to [Paul Bullock](https://twitter.com/pkbullock?s=20) for pointing this one out.
### [CodeTour](https://marketplace.visualstudio.com/items?itemName=vsls-contrib.codetour)

CodeTour is an awesome Visual Studio Code extension, which allows you to record and playback guided code walkthroughs. I’ve been using it to add tours to all my new web part projects and adding new tours to my old SPFx samples in the [Samples repo](https://aka.ms/spfx-webparts). ![CodeTour](../../images/post/uploads/2019/03/image-1594305617409.png)

## Nice to have

### [TeraCopy](http://codesector.com/teracopy)

If you’ve ever copied your SPFx project files, you know how frustratingly slow Windows can be. TeraCopy is insanely fast (so fast that you’ll think it didn’t work at first). Don’t take my word for it: next time you have to copy your SPFx project files, start your copy with Windows. Then, [download TeraCopy for Windows](http://codesector.com/teracopy), install it, and copy the exact same files using TeraCopy to a separate folder. Then go have a coffee, tell your co-workers that they should install TeraCopy, and go back to your desk. _Windows will still be copying the first set of files_. ![TeraCopy](http://codesector.com/img/teracopy/errors.png)

### [Zoomit](https://docs.microsoft.com/en-us/sysinternals/downloads/zoomit)

Be a considerate presenter! If you do presentations and show your code, you should consider installing this tool. Those people in the back of the room (who sat in the back so that they can exit quickly if they find you boring) may not exit so fast if they can actually see what you’re doing.

### [Paint.NET](https://www.getpaint.net/download.html)

A great image editing tool that’s fully featured and free. I use it to edit icons and other assets.

### [Inkscape](https://inkscape.org/)

A powerful SVG editing tool. I use it to create SVG icons. _If only I could [get SVG icons to work consistently in SPFx](https://github.com/SharePoint/sp-dev-fx-webparts/issues/766), it’d be great_.

### [SnagIt](https://www.techsmith.com/screen-capture.html)

Probably the golden standard for screen capture tools. I stubbornly used the Windows Snipping Tool for the longest time until I reluctantly installed SnagIt and I don’t think I’ll use anything but SnagIt from now on. If you write any kind of documentation, help guides, or blogs, this is a must.

### [Camtasia](https://www.techsmith.com/video-editor.html)

Like SnagIt, I used to avoid it because I was too cheap to pay for the license… but if you do any kind of video editing, give this one a try. It is fantastic. (Why do I have to be so stubborn?!)

### [ScreenToGif](https://www.screentogif.com/)

Do everyone a favour and show an animated GIF of what your SPFx solutions can do in the README.MD file. It saves them having to install your solution to see what it does. This tool is a screen, webcam and sketchboard recorder with an integrated editor that makes it super-easy to create animated GIFs. Available as a Microsoft Store App or a WPF install. ![ScreenToGif](../../images/post/uploads/2019/03/image-1562122087546.png)

## Browser Extensions

Note that these extensions can be used in Chrome or in Edge Chromium. (I use Edge Chromium, personally).

### [SP Editor](https://chrome.google.com/webstore/detail/sp-editor/ecblfcmjnbbgaojblcpmjoamegpbodhd)

A Google Chrome Extension for creating and updating files (js, css), injecting files to sites, modifying web/list property bag values (add, edit, remove, index) and creating webhook subscriptions, edit/add/remove web parts from publishing pages and run sp-pnp-js typescript snippets in SP2013, SP2016 and SharePoint Online from Chrome Developer Tools. This tool will help you create amazing SharePoint applications fast from your browser from any computer which runs Chrome!

### [React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)

Allows you to inspect the React component hierarchies in the Chrome Developer Tools. You get a new tab called **React** in your Chrome DevTools which shows you the root React components that were rendered on the page, as well as the subcomponents that they ended up rendering. It is great when trying to understand how the SharePoint team built a component.

### [Screen Reader for Google Chrome](https://chrome.google.com/webstore/detail/screen-reader-for-google/nddfhonnmhcldcbmhbdldfpkbfpgjoeh)

Test your web parts for accessibility by giving you the same experience your users will get when they use a screen reader.

### [AXE](https://chrome.google.com/webstore/detail/axe/lhdoppojpmngadmnindnejefpokejbdd)

No, not the body spray. Use this tool to check for accessibility for WCAG 2.0 and Section 508 accessibility. If you aren’t testing for accessibility, you’re possibly making it difficult for 10 to 20% of your users.

### [Refined GitHub](https://chrome.google.com/webstore/detail/refined-github/hlepfoohegkhhmjieoechaddaejaokhf)

If you use GitHub regularly, but get a little annoyed with some missing features, this extension is for you. It adds tons of cool features including my favorites: remove changes to individual files in a commit/pull request and download a folder. ![Enhanced GitHub in Action](../../images/post/uploads/2019/03/image-1599526636435.png)

### [SP Formatter](https://chrome.google.com/webstore/detail/sp-formatter/fmeihfaddhdkoogipahfcjlicglflkhg)

Not so much a developer-focused extension, but a very useful one nevertheless. SP Formatter adds JSON syntax highlighting, live preview, and autocompletion to SharePoint list formatting. ![SP Formatter](../../images/post/uploads/2019/03/image-1594304429322.png)

## Websites


### [PnP Home](https://pnp.github.io/)

Can’t keep up with all the new things that the Microsoft 365 PnP community members are doing? You can find everything in one convenient place. ![PnP Home](../../images/post/uploads/2019/03/image-1594304691913.png)

### [SharePoint Look Book](https://lookbook.microsoft.com/)

Get inspired with cool looking SharePoint sites. ![SharePoint Look Book](../../images/post/uploads/2019/03/image-1594304553898.png)

### [SharePoint Design Guidance](https://spdesign.azurewebsites.net/)

Learn how to create great looking SharePoint solutions. ![SharePoint Design Guidance](https://spdesign.azurewebsites.net/images/illustration.png?v=1)

### [Office Fluent UI](https://developer.microsoft.com/en-us/fluentui#/)

See what components are at your disposal when building awesome Office 365 solutions.

### [SharePoint Dev Platform Uservoice](https://sharepoint.uservoice.com/forums/329220-sharepoint-dev-platform)

Request new features and see what the team is working on.

### [PnP/PnPJS](https://pnp.github.io/pnpjs/)

PnPjs is a collection of fluent libraries for consuming SharePoint, Graph, and Office 365 REST APIs in a type-safe way. You can use it within SharePoint Framework, Nodejs, or any JavaScript project. This an open source initiative and we encourage contributions and constructive feedback from the community.

### [Reusable property pane controls for the SharePoint Framework solutions](https://sharepoint.github.io/sp-dev-fx-property-controls/)

This repository provides developers with a set of reusable property pane controls that can be used in their SharePoint Framework (SPFx) solutions. ![Reusable Property Pane Controls](https://pnp.github.io/sp-dev-fx-property-controls/assets/colorpicker-selector.png)

### [Reusable React controls for your SharePoint Framework solutions](https://pnp.github.io/sp-dev-fx-controls-react/)

Provides developers with a set of reusable React controls that can be used in SharePoint Framework (SPFx) solutions. The project provides controls for building web parts and extensions. You should really try the **ChartControl** 🙂 ![Reusable React Controls](https://pnp.github.io/sp-dev-fx-controls-react/assets/placeholder-intro.png)

### [Microsoft 365 & SharePoint Community – PnP (YouTube)](https://www.youtube.com/channel/UC_mKdhw-V6CeCM7gTo_Iy7w)

YouTube channel with SharePoint Dev Weekly videos, SharePoint Framework Tutorials and Training videos, SharePoint Framework and Extensions Tutorials, Getting Started videos, PnP Webcasts, etc. If you no like read, you watch these good.

### [Base64 Image Encoder](https://www.base64-image.de/)

Use this site to encode your web part icons to base 64. You can also use [my interactive post](https://hugoabernier.github.io//2019/08/31/fixing-base64-svg-icons-in-spfx/) to do all the work for you. ![Base64 Encoder](../../images/post/uploads/2019/03/image-1552589708483.png)

### [EzGif.com](https://ezgif.com/video-to-gif)

If you don’t want to install [**ScreenToGif**](https://www.screentogif.com/) but want to create animated GIFs to help people see what your web part will look like without having to install it, I recommend using this web site. Create a video of your web part in action, then use EZ GIF’s **Video to animated GIF converter** to create your GIF. Add the GIF to your README.MD file and people will see how cool your web part really is! ![EzGif](../../images/post/uploads/2019/03/image-1552589760776.png)

## GitHub Repos

### [Microsoft Fluent UI](https://github.com/microsoft/fluentui)

When I want to learn how to create awesome React components, I take my inspiration from Office UI Fabric Microsoft Fluent UI.

### [SP Dev FX WebParts](https://github.com/PnP/sp-dev-fx-webparts)

Almost every SPFx project I create starts from one of the many samples available on this awesome repo.

### [PnP Property Controls](https://github.com/PnP/sp-dev-fx-property-controls)

Back when most of us were still learning React and SPFx, they were already creating re-usable controls for SPFx. Take some time to read their code for inspiration.

### [PnP Developer Controls](https://github.com/PnP/sp-dev-fx-controls-react)

From the brilliant minds that brought you the PnP Property Controls. Read the code to learn tons!

### [SharePoint Starter Kit](https://github.com/PnP/sp-starter-kit)

Look at some of the best solutions used to build the perfect demo environments.

## Conclusion

This article listed the various tools I use when building SPFx solutions on a Windows 10 workstation. As I stated previously, I’m kind of a minimalist when it comes to installing stuff on my machine. I’m sure that there are many other tools that I should install, but I haven’t found a need for it yet. What other tools do you install on your workstation? Let me know in the comments.

## Update

* Feb 4, 2021: Added **SP Formatter VS Code Extension**. Mind.blown.
* September 7, 2020: Added **Enhanced GitHub**.
* July 9, 2020: Refreshed links and added **CodeTour**, **SP Formatter** and the **PnP Landing Page**.
* April 27, 2020: Added **Docs Authoring Pack**.
* December 06, 2019: Updated version of Node.js to 10.x.
* October 10, 2019: I added SPGo after attending [Beau Cameron](https://twitter.com/Beau__Cameron) and [David Warner II](https://twitter.com/DavidWarnerII)‘s great [SharePoint Saturday New England](https://spsnewengland.org/) session about SPFx Development Tips from the trenches. Watching those two present together reminded me that there is always room to learn more.
* July 2, 2019: Thanks to [Denis Molodtsov](https://twitter.com/Zerg00s) for suggesting ScreenToGif instead of using EzGif. It makes it so much easier to capture an animated GIF of your web part in action!
* April 4, 2019: Added SharePoint Developer Community – PnP YouTube channel
* March 28, 2019: Added \[Sergei Sergeev’s\] cool SPFx Typed Item extension, which he demoed in the March 28th SharePoint Dev Ecosystem call. Watch out for those Kung-fu Gophers.
* March 25, 2019: Thanks to Thomas Lamb for suggesting Prettier — Code Formatter.
* March 20, 2019: Thanks to [Sam Culver](https://twitter.com/samculver) for pointing out that Fira Code makes a great font in Visual Studio.
* March 16, 2019: Added Paint.NET and Inkscape as graphical tools.
* March 14, 2019: Thanks to Miguel Isidoro for pointing out that I had the wrong link to the Rencore SPFx Script Check.

## Credits

Header image by [Rudy and Peter Skitterians](https://pixabay.com/users/Skitterphoto-324082/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3129361) from [Pixabay](https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=3129361)

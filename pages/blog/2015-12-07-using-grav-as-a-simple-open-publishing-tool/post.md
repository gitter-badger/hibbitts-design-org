---
title: 'Using Grav as a Simple Open Publishing Tool'
slug: grav-as-a-simple-open-publishing-tool
date: '06-12-2015 00:00'
published: true
taxonomy:
    tags:
        - OpenPractice
metadata:
    'twitter:card' : summary
    'twitter:site' : @hibbittsdesign
    'twitter:title' : Using Grav as a Simple Open Publishing Tool
    'twitter:description' : An example of using Grav as a simple online publishing tool.
---

Recently, I've been exploring ways to use the modern flat-file CMS [Grav](http://getgrav.org/) as a simple open publishing tool. Grav is a natural candidate for this usage, as all content is stored as individual files which then can be placed on a variety of open and collaborative editing environments (e.g. GitHub).

Here is a snapshot of the approach with the best results so far:

* An instance of Grav running on a Web server, with the Admin Panel plugin installed and using the [Learn2](http://getgrav.org/downloads/themes) theme. The Learn2 theme has also been configured with the required GitHub repository URL information (see below). With the Admin Panel installed, any required updates for Grav can be done easily online.

  ![Grav Admin Panel Dashboard](dashboard.png)  
  _Figure 1. Grav Admin Panel Dashboard._

* A GitHub repository containing _only_ the "Pages" folder of the site. This results in having only content files (using Markdown) being presented in the repository, bringing a high-level of visibility to the content files of your site. You can view the GitHub repository of my "Pages" site folder at [https://github.com/hibbitts-design/course-companion-starter-kit](https://github.com/hibbitts-design/course-companion-starter-kit)  

  ![Example GitHub repository](course-companion-starter-kit-github.png)  
  _Figure 2. Example GitHub repository, containing only the "Pages" folder._

* Using a GetHub Webhook either through a service such as [Deploy](https://www.deployhq.com/), or directly by adding the needed PHP file (see [Grav Development with GitHub - Part 2](http://getgrav.org/blog/developing-with-github-part-2)), configure a site update to be automatically performed when one or more content files are modified on GitHub.

We now have a simple open publishing system operating! Anytime someone makes a change in the GitHub repository, and you approve of the change, the results will be automatically published to the live site. As well, all of your edits, etc. are available for public viewing and commentary. The content made available on GitHub may also be forked and used for other useful purposes.

It should be noted that you would want to make any significant changes to the chosen Grav theme  _before_ you upload the Grav site to your Web server. You can still make changes to the theme once it is running on your Web server, but doing so would require using a FTP program to edit the needed files or copy the updated files from your computer to the site. Alternatively, you could the place the entire "User" folder on GitHub which would also contain any theme modifications, but doing so would reduce the high-level visibility of your content files achieved when only placing the contents of your "Pages" folder on GitHub.

Here is an overview of the flow of making a change to content via GitHub:

1. Viewing the Grav site, a viewer can click the provided "Edit Page" link to propose changes to the page. You can view an example site at with the ability at [http://www.hibbittsdesign.org/coursecompanionstarterkit/](http://www.hibbittsdesign.org/coursecompanionstarterkit/)  

  ![Example site page - Overview](Overview.png)  
  _Figure 3. Example site page - Overview, using a modified version of the Learn2 theme with link to edit the page on GitHub._

2. Once the viewer has logged into GitHub, they can edit the page and then submit the Pull Request.
  ![Editing Overview site page on GitHub](Editing.png)  
  _Figure 4. Editing Overview site page on GitHub, which when completed will result in a Pull Request._

3. The site administrator reviews the submitted Pull Request, and can approve changes immediately or start a discussion with the author of the proposed changes for further modifications, etc.
  ![Review submitted Pull Request on GitHub](PullRequest.png)  
  _Figure 5. Review submitted Pull Request on GitHub, showing GitHub's super-useful file changes preview._

4. Once the change has been approved by a site administrator of the GitHub account, and the changes to the GitHub repository have been automatically pushed to the server, the updated content is available to be viewed.
  ![Updated site page - Overview](UpdatedOverview.png)  
  _Figure 6. Updated site page - Overview._

I personally also like to use [GitHub Desktop](https://desktop.github.com/) as a point-and-click means to keep a local copy of my GitHub repositories on my local machine so I can use any markdown-enabled application when editing my content files. You can learn more about my use of GitHub Desktop in my earlier post [My Dream Workflow as an Instructor](http://hibbittsdesign.org/blog/my-dream-workflow-as-an-instructor).
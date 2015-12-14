---
title: 'Using Grav with GitHub Desktop (and Deploy)'
slug: using-grav-with-github-and-deploy
date: '13-12-2015 00:00'
published: true
taxonomy:
    tags:
        - OpenPractice
        - GitHub
        - GravCMS
        - FlatFileCMS
metadata:
    'twitter:card' : summary
    'twitter:site' : @hibbittsdesign
    'twitter:title' : Using Grav with GitHub Desktop and Deploy
    'twitter:description' : How to use Grav with GitHub Desktop and Deploy.
---

As a modern flat-file CMS, [Grav](http:getgrav.org) can take full advantage of today's ecosystem of open and collaborative editing services, such as [GitHub](http://github.com) or [GitLab](http://gitlab.com). In this article we will look at how to easily use Grav with GitHub and the automatic deployment service [Deploy](http://www.deployhq.com) to result in a very efficient, open and collaborative workflow. No scripting or command line interactions will be required.

As an educator, the use of GitHub to store (not host) an online course companion is very appealing as not only does it support an open practice but also enables students to control the very learning environment that they are using! I first described this workflow in my earlier article [My Dream Workflow as an Instructor](../my-dream-workflow-as-an-instructor).

Before you start this tutorial I suggest you first get your Grav site up and running locally using [MAMP](https://www.mamp.info/en/), as outlined in [Running Grav Locally with MAMP](../running-grav-locally-with-mamp).

This tutorial should take about 15 minutes, and once completed you will have an efficient, open, and collaborative workflow for yourself and _your students_! It's 15 minutes that can forever change your day-to-day workflow for your Grav course companion sites.

**Step-by-step instructions**

1. If you do not done so already, [sign up for a GitHub account](https://github.com/join).

2. Download the [GitHub Desktop](https://desktop.github.com/) client for your computer (Mac or PC), and once it is installed launch the application and proceed with the setup process to enter your GitHub account credentials.

  ![GitHub Desktop setup welcome](github-desktop-welcome-1.png)  
  _Figure 1. GitHub Desktop setup welcome._

  ![GitHub Desktop connect to GitHub](github-desktop-welcome-2.png)  
  _Figure 2. GitHub Desktop connect to GitHub._

3. Assuming you already have a Grav site present on your computer (and preferably one that is already viewable via MAMP), you next need to create a GitHub Repository of your site. It is recommended that if this is the first time you are using GitHub with Grav that you add the entire Grav site to GitHub, but other approaches are possible such as only storing the "user" folder (see the provided additional resources at the end of this article for more options).

  ![GitHub Desktop main window](github-desktop-main-window.png)  
  _Figure 3. GitHub Desktop main window, displaying the included tutorial._

  Press the "Add a Repository" button (upper-right plus(+) sign in the main window) in the GitHub Desktop client, select the "Add" tab within the displayed dialog box, and then press the "Choose..." button to select the folder containing your _entire_ Grav site.

  ![GitHub Desktop add Repository dialog](github-desktop-add-repository-dialog.png)  
  _Figure 4. GitHub Desktop add Repository dialog._

  ![GitHub Desktop local Repository added](github-desktop-local-repository-added.png)  
  _Figure 5. GitHub Desktop local Repository added._

4. You are now ready for the first commit to your new GitHub repository. Whenever you make a commit you will need to include a brief text summary - as this is your first commit enter the text "First commit." into the "Summary" text box, and then press the button "Commit to master".

  ![GitHub Desktop first commit](github-desktop-first-commit.png)  
  _Figure 6.  GitHub Desktop first commit._

5. Since this is your first commit to your repository, the "Publish" button (upper-left of main window) will need to be also pressed to actually perform the actual file updates. Once the "Publish" button is pressed enter a short description for your new GitHub repository and then select which GitHub account you want to publish to (if you have multiple accounts).

  ![GitHub Desktop repository details dialog box](github-desktop-publish-repository.png)  
  _Figure 7. GitHub Desktop - repository details dialog box._

  ![GitHub Desktop publishing the repository](github-desktop-publishing-the-repository.png)  
  _Figure 8. GitHub Desktop publishing the repository._

  ![GitHub Desktop - repository published](github-desktop-repository-published.png)  
  _Figure 9. GitHub Desktop repository published._

6. Once this process is complete you should now be able to view your Grav site files stored on GitHub - please do this now to ensure that everything went as expected. If you have any issues during this process you may find more detailed GitHub Desktop client support information at [https://help.github.com/desktop/](https://help.github.com/desktop/).

  ![GitHub repository of your Grav site](github-repository.png)  
  _Figure 10. GitHub repository of your Grav site._

7. To maximize the benefit of using GitHub to store your Grav site files, you can use various tools and techniques to trigger an automatic deployment of any changed GitHub files to your live site hosted on a Web server. To make this step as easy as possible, I recommend you use one of the various Web services that provide this functionality - such as [Deploy](deployhq.com).

  ![Deploy website homepage](deploy.png)  
  _Figure 11. Deploy website homepage._

  Head over to [Deploy](deployhq.com), and sign-up for a free account (one project, up to ten commits per day). Once you have signed up then create a new project with the needed details of your GitHub repository information and your web server credentials.

  ![Deploy account welcome page](deploy-welcome.png)  
  _Figure 12. Deploy account welcome page._

8. With your first Deploy project created and configured, you will need to get the Webhook URL needed to be added to your GitHub repository for automatic deployment of any changed site files. Press on the "Server" button of your project info box to view the Server details page.

  ![Deploy projects page](deploy-projects.png)  
  _Figure 13. Deploy projects page._

9. Next, on the Server details page press the pencil (edit) icon.

  ![Deploy servers page](deploy-servers.png)  
  _Figure 14. Deploy servers page._

10. On the far right-hand side of the "Edit Server" page the URL for "Automatic Deployments" is displayed - select the text of this URL and then copy to your clipboard.

  ![Deploy edit server page](deploy-edit-server.png)  
  _Figure 15. Deploy edit server page._

9. With the automatic deployment URL copied to your clipboard, you now need to add that URL as a Webhook to GitHub. Navigate to your GitHub Repository, press "Settings" and then press "Webhooks & services".

  ![GitHub repository settings](github-settings.png)  
  _Figure 16. GitHub repository settings._

  ![ GitHub repository settings - Webhooks & services](github-settings-webhook.png)  
  _Figure 17. GitHub repository settings - Webhooks & services._

10. Paste the URL that you copied from your Deploy project server settings, choose "application/x-www-form-urlencoded" in the "Content type" drop-down menu and then press the "Add webhook" button.

  ![GitHub repository settings - Webhooks & services information updated.](github-settings-webhook-entered.png)  
  _Figure 18. GitHub repository settings - Webhooks & services information updated._

  ![itHub webhook information saved](github-webhook-added.png)  
  _Figure 19. GitHub webhook information saved._

Congratulations! With the above steps completed you now have a Grav site which you can run and test locally (using MAMP), and with _only one click_ in the GitHub Desktop application have any changed local site files updated in your GitHub repository and then have them automatically pushed to your Web server hosting your Grav site. In my experience, I can make an update to my Grav site and sync changes to GitHub for automatic deployment to my Web server in as little as 30 seconds.

  ![ GitHub Desktop repository changes screen](github-desktop-repository-sync.png)  
  _Figure 19. GitHub Desktop repository changes screen. When any changes are detected they will be displayed on this screen and can be pushed to GitHub when the "Commit and Sync master" button is pressed._

Students can also now make suggested changes to your Grav site via GitHub or GitHub repository file links provided in your Grav site (see the bottom of this example page at [http://cmpt-363-153.hibbittsdesign.com/resources](http://cmpt-363-153.hibbittsdesign.com/resources)). GitHub will provide an excellent view of proposed changes, which you can immediately accept or start a further discussion about these possible changes with the student submitting them.

You can press the GitHub Desktop client "Sync" button (which replaces the "Publish" button you previously used) in the GitHub Desktop client to also download any changes made to the online GitHub repository down to your own computer.

Interested in learning even more about using Grav with GitHub? Check out these two super-informative posts on the Grav Blog:
* [Grav Development with GitHub - Part 1](http://getgrav.org/blog/developing-with-github-part-1)
* [Grav Development with GitHub - Part 2](http://getgrav.org/blog/developing-with-github-part-2)

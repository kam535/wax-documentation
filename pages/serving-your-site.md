---
title: Serving your site
layout: default
parent: Setting up your site
nav_order: 5
---
## **Serving your site**
1. TOC
{:toc}

You can serve your site in many ways, but two in particular are included in this documentation: locally or through GitHub Pages. If you choose to serve your site locally, note that it will not be available on the World Wide Web. Serving locally serves the purpose of checking your site before you publish it publicly online. For instructions on serving your site, see the [Serving your site section](https://minicomp.github.io/wiki/wax/serving/) of the Wax documentation.

**Note that some of the following content is copied from the Minicomp Wax Documentation and should be credited to [Minicomp](https://minicomp.github.io/wiki/)**.

### **Serving locally for development**
If you’re running Wax directly on your machine, serving *should* be as simple as `bundle exec jekyll serve`.
<br>
If you’re in a Docker container, you’ll need to specify the host: `bundle exec jekyll serve --host 0.0.0.0`.

## **Hosting / publishing online**
There are many options. Our demo uses GitHub pages. You can use any hosting service of your choice, but the Wax demo uses GitHub Pages, which allows you to serve and host a site for free in a GitHub repository. 

### **Hosting on GitHub Pages**
If you have a wax site repository that you want to publish to GitHub pages:
1. Push your changes to GitHub.com. You can follow [this documentation's instructions for pushing your changes to GitHub.com](https://kam535.github.io/wax-documentation/pages/pushing-your-changes.html)
2. Open your repository on GitHub.com.
3. Go to **Settings** or click the gear icon. Click on **Pages** on the left sidebar.
4. Under **Source**, select "Deploy from a branch". Then select the “main” branch and “root” folder. Click “Save”.
5. In the top menu of your repository, click **<> Code**.
6. On the right side of the screen, click the gear icon next to “About”.
7. Under website, check the box that says “Use your GitHub Pages website”. Click the green Save changes button.
8. The URL that now appears in the “About” section is your new website URL.

### **Updating your site configurations**
1. Open your **_config.yml** file.
2. Replace the url field with your own url, e.g., https://your-username.github.io. Omit the period at the end.
3. Replace the baseurl with your own baseurl, which will be the same as your repository name, e.g., /your-repo-name.

<img src="https://kam535.github.io/wax-documentation/images/site-screenshot.png" alt="screenshot of the Wax demo site homepage">

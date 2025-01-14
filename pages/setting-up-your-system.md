---
title: Setting up your system
layout: default
nav_order: 3
---

1. TOC
{:toc}
   
## **Setting up your system**
Since Wax uses your local machine to produce all of the static site pages and elements in HTML, CSS, and Javascript, using Wax requires you to install dependencies on your machine. This documentation will only include the full text and an extension of Minicomp's [Manual Installation Guide](https://minicomp.github.io/wiki/wax/setting-up-your-system/install-manually/). If you wish to use Docker, please see the [Docker Installation Guide](https://minicomp.github.io/wiki/wax/setting-up-your-system/with-docker/). 

**Note that some of the content below has been copied from the [original Wax documentation](https://minicomp.github.io/wiki/wax/) and can be credited to Minicomp and its contributors.**

### Requirements
* [Homebrew](https://brew.sh) (on Mac OS)
* [Ruby](https://www.ruby-lang.org/en/) (a recent version); this version should be set up so that it does not conflict or overwrite your system's endemic Ruby version. See [rbenv](https://rbenv.org) or [RVM](https://rvm.io) for details
* Bundler (as part of your Ruby installation)  
* [Image Magick](https://imagemagick.org/script/download.php)  
* [Ghostscript](https://www.ghostscript.com/)
* [Git](https://git-scm.com/)
* [libvips](https://libvips.github.io/libvips/)
* [GitHub Desktop](https://desktop.github.com/download/)
* 
<img src="https://kam535.github.io/wax-documentation/images/depen.png" alt="logos for GitHub Desktop, Git, Ruby, Image Magick, GhotScript, and Homebrew and a lightning bolt icon">

### Installing on Mac
1. Open the Terminal.
  - If you've never used the Terminal before, open the **Applications** folder on your Mac. Open the **Utilities** folder and find **Terminal.app**.
2. Check to see if you have Homebrew installed by pasting `brew -v` into the command line and pressing the **return** key.
  - If you do not have [Homebrew](https://brew.sh) installed, run the following command:
    `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`.
    Follow the [Homebrew installation instruction](https://brew.sh).
3. Install Git and Gnupg by running the following command:
`brew install git gnupg`
4. Install Ghostscript, libvips, and ImageMagick by running the following command:
`brew install imagemagick ghostscript libvips`
5. Lastly, install Ruby using RVM by running the following commands:
`gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
`\curl -sSL https://get.rvm.io | bash`
6. Quit and reopen the terminal. Then run the following command to get a Ruby version that comes with Bundler:
`rvm install 2.7.2`
7. Install GitHub Desktop by going to the [download page](https://desktop.github.com/download/) and following the instructions.
  - If you do not already have a GitHub account, make one by following the [signup instructions](https://github.com/signup).

### Installing on Windows
1. Install Ruby by following the [Ruby Installer for your Windows version](https://rubyinstaller.org). On the last installation step make sure to run the `ridk install` step on the last step of the installation wizard.
2. Install Git for Windows, following the [installation guide](https://git-scm.com/downloads/win).
3. Install Image Magick for Windows, following the [installation guide](https://imagemagick.org/script/download.php#windows).
4. Install Ghostscript Postscript and PDF interpreter/renderer, following the [Download page instructions](https://ghostscript.com/releases/index.html).
5. Download and open the libvips `.zip` file from the [libvips GitHub page](https://github.com/libvips/libvips/releases/tag/v8.11)
6. Install GitHub Desktop by going to the [download page](https://desktop.github.com/download/) and following the instructions.
  - If you do not already have a GitHub account, make one by following the [signup instructions](https://github.com/signup).

When you're done installing everything, check the requirements to make sure you've got all your dependencies installed.

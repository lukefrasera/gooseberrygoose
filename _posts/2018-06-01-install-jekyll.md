---
layout: article
title: A Stroll in Moses, Lake
header:
  theme: dark
  background: 'linear-gradient(135deg, rgb(34, 139, 87), rgb(139, 34, 139))'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /assets/images/bg.jpg
---

In this example we will break down creating a new post on your computer. We will cover installation, editing and release. The descriptions will be brief, but should provide a sort of guideline for managing your website. This page will give you the necessary tools to edit and post content to your website. Let's get started!

# Installation

## Windows (Windows Subsystem for Linux)

This section provides step-by-step instructions on the setup required to test your website locally. You program the site and view it locally in a browser. This will make more sense later. For now we need to install several programs to help us run the website locally.

![website_screenshot]({{site.url}}/assets/images/website_screenshot.png){:.border}

### WSL: Windows Subsystem for Linux

The main issue with windows is its inability to make running a server easy. More specifically most of the internet prefers opensource alternatives. A common developer platform is linux. Thankfully, recently microsoft ended its war on linux and decided to integrate the operating system into itself. This allowed users on windows to run software that was built for linux.

In the case of your website we will be using a technology called Jekyll. Jekyll is a static website builder and is an accepted base for websites on github. Using Jekyll your website can be hosted for free on github.com. Once setup you can forward traffick from you personal URL to the github.com url. Jekyll is a linux program. To install it we need to enable some windows 10 special features.

#### Enable Linux Subsystem Feature

press the **Windows** key and type: `turn windows features on`

![enable wsl]({{site.url}}/assets/images/windows_subsystem.png)

Select the item at the top of the list. The window below should show up and you can scroll down to find a checkbox labeled `Windows Subsystem for Linux`. Check this box and press ok! This will take some time to finish installing the necessary dependencies. After the installation is complete restart your computer.

#### Install Ubuntu 18.04

Next we will install a version of linux called `Ubuntu`. Specifically we are installing version `18.04` of `Ubuntu`. To do this first open the windows store.

1. Open the windows store.
2. Search for: `Ubuntu`
   1. You should see several options.
3. Select `Ubuntu 18.04` option from the store and install.

![windows store]({{site.url}}/assets/images/windows_store_ubuntu.png)

![windows store ubuntu]({{site.url}}/assets/windows_store_1804.png)

Once Ubuntu is installed you are ready to initialize it on your computer.

1. Press the windows key and type: `ubuntu`
2. Launch the `ubuntu` application
![start menu]({{site.url}}/assets/images/start-menu.png)

3. Setup your username
   * Enter your desired username for your ubuntu instance. Keep it short and simple. Something like your name is usually preferred.
![username]({{site.url}}/assets/images/ubuntuinstall.png)
4. Create a password. Keep it somewhat simple.

Congrats!! You have successfully installed `Ubuntu` on your windows installation. Now we can install the remaining dependencies and begin building your website.

### Ruby

The next step to building your website locally is installing `Ruby`. Ruby is an older language used predominately with web technologies.

### npm

### Jekyll

## Install Mac - OSX

The Mac installation is much more simple. To install jekyll on mac we will first open up a terminal this can be done by opening the search bar and typing terminal. when you have opened the terminal we can begin.

### Install Home Brew

In the terminal you will type these commands:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

This will setup homebrew on your system.

### Install ruby

In the terminal you will type these commands:

```bash
brew install ruby
```

Next we will setup an environment variable to make using ruby much easier from the terminal..

```bash
echo export PATH=/usr/local/opt/ruby/bin:$PATH >> ~/.bashrc
exit
```

The above commands will result in the terminal window closing. You will want to reopen a new terminal window now. This was necessary to reload the terminal environment to include the change we just made.

Now, lets verify that the installation was successful.

```bash
ruby -v
```

This should output a result that shows the current version of ruby. Otherwise, you will get an error.

### Install Jekyll

We will use the ruby install from before to install jekyll

```bash
gem install --user-install bundler jekyll
```

Now you should be all set to work with jekyll on your computer.

Next you will want to [install git]({% post_url 2019-08-26-install-git %})

<!--more-->

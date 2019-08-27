---
layout: article
title: Install/Configure Git
header:
  # theme: dark
  # background: 'linear-gradient(135deg, rgb(175, 234, 255), rgb(125, 255, 0))'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(0, 153, 255 , .3), rgba(255, 255, 0, .2))'
    src: /assets/images/bg.jpg
---

# Install Git on Mac

To install git we will use homebrew installed in the previous tutorial.

```bash
brew install git
```

That is it you have now installed git.

## Configure git

First we will setup our git configuration with our email address and username:

```bash
git config --global user.name "Erin Hummel"
git config --global user.email "replace with your preferred email address"
```

## Configure github credentials

Next we want to make it so we don't have to enter a password each time we update the site.

```bash
ssh-keygen -b 4096
```

You will be prompted by questions. You may skip all of them by pressing the `<enter>` several times. Now we generated our key we can use it on github to authenticate our computer.

```bash
cat ~/.ssh/id_rsa.pub | pbcopy
```

Now your public key in on your clipboard. Lets login to github and go to our account settings:

![github settings]({{site.url}}/assets/images/guthub-settings.png)

Your view will look very different from mine. I have customized my view and I have many repositories. The important part is in the top right corner. There you will click on settings.

![github settings page]({{site.url}}/assets/images/github-settings-page.png)

Click on `SSH and GPG keys`. There you will click `New SSH key`. This will prompt for inputting the new SSH key.

![new ssh key]({{site.url}}/assets/images/github-new-ssh-key.png)

For the `Title` you should give it a nickname for your current computer. In the key text field you will paste your clipboard into the cell. You can then confirm the new key by clicking `Add SSH key`. You have successfully authenticated your machine.


## Clone Website

Now that we have setup git on your computer, you can download your website to your computer. When using git this is called cloning.

```bash
git clone git@github.com:lukefrasera/gooseberrygoose.git
```

This will have downloaded your website to `gooseberrygoose` in your current directory.

```bash
cd gooseberrygoose
npm run serve
```

The server should now start. You can access it locally in a web browser at the url: [localhost:8000](localhost:8000)


I am sure you will have questions while going through this tutorial. Please email me any issues or questions at luke@fratkins.com.

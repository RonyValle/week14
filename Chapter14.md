#  How To Change Your Window Manager

## Introduction

        Your Computer's *GUI* (Graphical User Interface) must relay on two very important components to create
either floating or tilling windows for every application you open. The core of this can be traced back to
the X window system server. X windows manages everything from rendering windows to configuring display handling
input from devices such as keyboards and mice. All the applications relying on the X server are clients.
They must talk to X in order to figure out where to place their windows and the rendering of them. X clients
can also provide services to other clients, this is where a *window manager* comes into play. The window manager
is one of the most important client service applications because it figures out how to arrange windows on the screen
and also provides title bars, closing, minimizing, and maximizing of windows as well as moving the window around on the screen.

        This is somewhat of a tutorial on how to change your window manager in Ubuntu. I am running Ubuntu 16.04.3 LTS
to a accomplish this task. Also the window manger I will install is called awesome. So what is Awesome? as put by the Awesome
official website <https://awesomewm.org> awesome is a highly configurable, next generation framework window manager for X.
It is very fast, extensible and licensed under the GNU GPLv2 license. It is primarily targeted at power users, developers and
any people dealing with every day computing tasks and who want to have fine-grained control on their graphical environment.

### Lets get started!

1. First thing we should do is to update the repository. Ubuntu uses *apt-get* for its package manager
   I will be using it here. The following command updates the repository:
   `apt-get update` **[Make sure to run all this commands as sudo if not logged in as root]**
2. Search for all the packages that have the name awesome with this command:
   `apt-cache search awesome`
3. The one you want to install should say this:
   `awesome - highly configurable X window manager`
4. If this option shows up after you run the command on step 2, Everything is going good for you.
   If you don't get this results make sure you are connected to the Internet.
5. To install awesome we will run the proper command using sudo rights:
   `apt-get install awesome`
   This will take some time so let it do its thing.
6. Once installed, you can reboot or log out of your current session. To get back to the log in screen.
7. On the log in screen you see a window that displays your user name on one corner and a tiny
   Ubuntu logo on the other. Click on this logo. The window now reads *Select Desktop Environment*
8. Choose the one that reads awesome.
9. Log In, you are now presented with the awesome window environment..enjoy!

Here are some links to learn more about Awesome and its features:

<https://awesomewm.org/doc/manpages/awesome.1.html>

<https://scaron.info/blog/getting-started-with-awesome.html>

#### Thanks for reading!

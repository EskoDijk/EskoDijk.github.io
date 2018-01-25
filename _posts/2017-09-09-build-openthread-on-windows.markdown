---
layout: post
title:  "Build OpenThread on Windows using Cygwin"
date:   2017-09-09 19:42:00 +0100
categories: thread simulation
---
The open source Thread wireless mesh networking stack [OpenThread](https://openthread.io/) contains a nice option to build simulated Thread nodes than can run on your PC. This [Google codelabs exercise](https://codelabs.developers.google.com/codelabs/openthread-simulation) explains in more detail how this can be used to simulate a very simple Thread network consisting of 2 nodes. A Linux VM is used to run the simulated nodes. Now wouldn't it be great to just run your simulated nodes directly in Windows 10 as .exe executables? One way to get there is to build openthread in the Cygwin environment.

In Cygwin, the following packages need to be installed first:

{% highlight bash %}
automake
autoconf
python2
pip for Python 2
gcc
g++
libtool
{% endhighlight %}

Note that pip can be named "pip2" or "pip". For Python you need the package "pexpect". Install it from bash using:

{% highlight bash %}
pip2 install pexpect
{% endhighlight %}

If you don't have the openthread repo from Github already, clone it into a directory of choice:

{% highlight bash %}
git clone https://github.com/openthread/openthread.git
cd openthread
{% endhighlight %}

To make sure that line endings are UNIX style, cd to your openthread repo and use the below. Don't use this if your openthread repo contains local changes!

{% highlight bash %}
git config core.autocrlf false
git rm --cached -r . && git reset --hard
{% endhighlight %}

The repository can be prepared for building using the bootstrap script.

{% highlight bash %}
./bootstrap
{% endhighlight %}

Have a look at the output. It should complete without errors. (Errors may point to some missing tool/dependency or presence of Windows style line endings.) Now the POSIX example programs can be built using:

{% highlight bash %}
make -f examples/Makefile-posix
{% endhighlight %}

After building, the [codelabs exercise](https://codelabs.developers.google.com/codelabs/openthread-simulation/index.html#2) to start 2 simulated nodes in separate shell windows can be followed. Using a command like below the first Full Thread Device (FTD) can be started:

{% highlight bash %}
./output/x86_64-unknown-cygwin/bin/ot-cli-ftd.exe 1
{% endhighlight %}

and in another window a second one:

{% highlight bash %}
./output/x86_64-unknown-cygwin/bin/ot-cli-ftd.exe 2
{% endhighlight %}

the default Thread network can be started by a sequence of commands, to be run in both shell windows:

{% highlight bash %}
ifconfig up
panid 0x1234
thread start
{% endhighlight %}

To confirm the nodes are attached to the network the 'state' command can be used. And finally scan the virtual airwaves and wonder where the developers did get their lunch!

{% highlight bash %}
> scan
| J | Network Name | Extended PAN | PAN | MAC Address | Ch | dBm | LQI |
+---+------------------+------------------+------+------------------+----+-----+-----+
| 0 | OpenThread | dead00beef00cafe | 1234 | fa5b112e46122b2f | 11 | -20 | 0 |
Done
{% endhighlight %}

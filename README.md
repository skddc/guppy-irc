guppy-irc
=========

A tiny embeddable IRC client, using the open-source [sockethub service](http://sockethub.org).

use
===

To use guppy-irc you must include a few `.js` files and define the guppy widget:

  ...
  <guppy-irc id="myGuppy"
             data-title="Welcome to Guppy IRC"
             data-width="80"
             data-height="28"
             data-server="*[irc server hostname]*"
             data-channel="*[#irc_channel]*"
             data-nick="guppy_user"
             data-display-name="Guppy Example User"
             data-password=""
             data-sockethub-host="*[sockethub hostname]*"
             data-sockethub-port="*[port number]*"
             data-sockethub-tls="*[true | false]*"
             data-sockethub-path="*[/path]*"
             data-sockethub-secret="*[connect string]*" />

  ...
  <script src="sockethub-client/sockethub-client.js"></script>
  <script src="../src/js/guppy-irc.js"></script>
  ...

dependencies
============

Guppy IRC uses Sockethub for IRC connectivity, and therefore has the following
dependencies:

* [sockethub-client.js](http://github.com/sockethub/sockethub-client)

* A running [Sockethub](http://github.com/sockethub/sockethub) instance.

status
======

Guppy IRC currently has basic functionality. You can connect to a channel, and
send/receive messages. The UI still needs lots of love.

Also, the Sockethub IRC platform is still under heavy development, as it becomes
more stable so should Guppy. However right now things appear to be functional
stable at it's basic element, if lacking in features.


example
=======

### live demo

You can try out Guppy IRC, which is connecting to a public sockethub instance
and automatically connects to the #sockethub channel, here:

[http://silverbucket.github.io/guppy-irc/example/](http://silverbucket.github.io/guppy-irc/example/)


### run your own demo

To get the Guppy IRC example up and running, do the following.

    $ git clone https://github.com/silverbucket/guppy-irc.git
    $ cd guppy-irc
    $ git submodule update --init
    $ python -M SimpleHTTPServer 8000

Then browse to `localhost:8000/example`, you should see the example load in your
browser.
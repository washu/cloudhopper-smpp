Cloudhopper by Twitter
============================

cloudhopper-smpp
------------------------

Efficient, scalable, and flexible Java implementation of the Short Messaging
Peer to Peer Protocol (SMPP). This library supports the following SMPP protocol
versions:

 - 3.3
 - 3.4
 - most of 5.0

This library's implementation takes advantage of non-blocking (NIO) sockets to
support thousands of binds using minimal resources.  It can be used to
implement either the server, client, or both sides of the SMPP protocol. We use
it internally at Twitter for both.  Both synchronous or asynchronous request
modes can be supported on an SMPP session.

The library has been tested and certified with hundreds of mobile operators
and suppliers around the world.  It's effective at being flexible with SMPP
specifications that aren't truly compliant.

SMPP is notorious for having slight differences depending on the vendor. This
library attempts to ensure that the internal PDU parser never breaks regardless
of vendor.

Contributors
------------

Joe Lauer (Twitter: [@jjlauer](http://twitter.com/jjlauer))

Installation
------------

Library versions >= 5.0.0 are now published to the Maven Central Repository.
Just add the following dependency to your project maven pom.xml:

    <dependency>
      <groupId>com.cloudhopper</groupId>
      <artifactId>ch-smpp</artifactId>
      <version>[5.0.0,)</version>
    </dependency>

Demo Code / Tutorials
---------------------

There are numerous examples of how to use various parts of this library:

    src/test/java/com/cloudhopper/commons/util/demo

To run some of the samples, there is a Makefile to simplify the syntax required
by Maven:

    make client
    make server
    make performance-client
    make simulator
    make rebind
    make parser
    make dlr

On Windows, the examples can run with `nmake` instead of `make`.

The easiest way to get started is to try out our `server` and `client` examples.
Open up two shells.  In the first shell, run:

    make server

In the second shell, run:

    make client

You'll see the client bind to the server and a few different type of requests
exchanged back and forth.

License
-------

Copyright (C) 2010-2012 Twitter, Inc.

This work is licensed under the Apache License, Version 2.0. See LICENSE for details.
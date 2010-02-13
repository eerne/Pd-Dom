Pd-Dom
======

aka. pure dynamic object model

Pd-Dom is a wrapper around the unofficial Pd dynamic object methods. It is an abstracted layer that simplifies API to dynamically chain objects (Pd-abstractions) in a node structure. Trees can be build with multiple nested Pd-Dom instances. Objects are given a unique Id as $1 argument and use globally available send~ and receives~. It currently is built on vanilla Pd and later optionally on dyn~ with the same API. All methods are zero based.

[Read more about Puredata aka Pd on crca.ucsd.edu/~msp/software.html](http://crca.ucsd.edu/~msp/software.html)

How to use
----------

	[pd-dom Foo]

### Messages

 * add <plugin> [<arg1> [<arg2> ...]]
 * set <position> <plugin>
 * del <position> [<position2> [<position3> ...]]

see subpatch [pd more]

### Internals

<id>.nodes
<id>.nodes.get
<id>.nodes.set

<id>.tree
<id>.node.<no>
<id>.bin.<no>

Todo
----

 * fix reset bug
 * fix exmaples
 * code review
 * build dyn~ wrapper
 
 
Author(s)
---------

 * Enrique Erne
 
License
-------

Copyright (c) 2009-2010, Enrique Erne

Licensed under the MIT license: http://www.opensource.org/licenses/mit-license.php

[pdom] is inspired by the [mMm](http://puredata.info/Members/eni/mMm) project. 

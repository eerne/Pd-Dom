Pd-Dom
======

aka. pure dynamic object model for **Puredata**

Pd-Dom is a wrapper around the unofficial Pd dynamic
patching methods. It simplifies API to create and chain abstractions.
Tree structures can be build with multiple nested Pd-Dom instances.
Objects are given a unique Id as \$1 argument and use globally available
send~ and receives~. There are plans to support [dyn~] as well. All
methods are zero based.

Read more about [Puredata aka Pd on crca.ucsd.edu/~msp/software.html](http://crca.ucsd.edu/~msp/software.html)

How to use
----------
	[add myRandomSeq, add myInstrument, add myEffect(
	 |
	[pd-dom <id>]
	 |
	[dac~]

### Methods

	add <plugin> [<arg1> [<arg2> ...]]
	set <position> <plugin>
	del <position> [<position2> [<position3> ...]]

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
 * code review
 * build dyn~ wrapper
 
 
Author(s)
---------

 * Enrique Erne
 
License
-------

Copyright (c) 2009-2010, Enrique Erne

Licensed under the [MIT license](http://www.opensource.org/licenses/mit-license.php)

**Pd-Dom** is inspired by the [mMm](http://puredata.info/Members/eni/mMm) project. 

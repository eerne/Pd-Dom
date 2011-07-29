Pd-Dom
======

aka. pure dynamic object model for **Puredata**

Pd-Dom is a wrapper around the unofficial Pd dynamic
patching methods. It simplifies API to create and chain abstractions.
Tree structures can be build with multiple nested Pd-Dom instances.
Abstractions are given a unique Id as \$1 argument and use globally available
send~ and receives~ and automatically listen to the previous node. 
There are plans to optionally wrap [dyn~] with same API. All methods are zero based.

Read more about [Puredata aka Pd on crca.ucsd.edu/~msp/software.html](http://crca.ucsd.edu/~msp/software.html)

How to use
----------
	[adc~]
	 |	  [add aSequencer, add myInstrument, add someEffect(
	 |	   /
	[pd-dom <id>]
	 |
	[dac~]

### Methods

	add <abstraction>
	chain <abstraction> [<abstraction> [<abstraction> ...]]
	set <position> <abstraction>
	delete <position> [<position> [<position> ...]]
	vis <position>
	reset

### Methods (proposal)

	add <abstraction> [<arg2> [<arg3> ...]]

see subpatch [pd more]

### Reserved receivers (internals)

	<id>
	<id>.nodes
	<id>.nodes.get
	<id>.nodes.set
	<id>.nodes~
	<id>.nodes~.get
	<id>.nodes~.set
	
	<id>.bin
	<id>.bin.<number>

	<id>.<number>
	<id>.<number>.vis
	<id>.node.<number>

Todo
----

 * refactoring 
 * build dyn~ wrapper


Author(s)
---------

 * Enrique Erne

License
-------

Copyright (c) 2009-2011, Enrique Erne

Licensed under the [MIT license](http://www.opensource.org/licenses/mit-license.php)

**Pd-Dom** is inspired by the [mMm](http://puredata.info/Members/eni/mMm) project. 


=====================
Awesome rmdir command
=====================

If you don't use the ``rmdir`` command you can stop reading here and `go watch
some kpop instead <http://www.youtube.com/watch?v=dEf4PJZXBxA>`_.

But if you use the ``rmdir`` command in a desktop like environment you may
*hate* that it won't remove directories which contain files like ``.DS_Store``
or ``Thumbs.db``, which modern OSes create everywhere and make you cringe every
time you have to deal with them.

The ``awesome_rmdir`` command is a reimplementation of the trusty ``rmdir``
command in the `Nimrod programming language <http://nimrod-lang.org>`_. It
first tries to remove the directory as usual, and only if normal removal fails
it will scan the directory and remove these *useless* files, then try again the
removal of the directory you specified. The end result should be that if the
directory is *acceptably empty* it will be removed.

Removal of the directory follows ``rmdir`` tradition and will remove the
directory immediately without putting it in the recycle bin. If you need
recycling of files from the command line you could use the `trash-binary
<https://github.com/gradha/genieos/tree/master/trash-binary>`_ from the
`genieos Nimrod module <https://github.com/gradha/genieos>`_ instead.

I should work in marketing.


License
=======

`MIT license <LICENSE.rst>`_.


Installation and usage
======================

You are meant to know what you are doing, so this will be brief:

* Install `Nimrod <http://nimrod-lang.org>`_.
* Install `Nimrod's babel package manager
  <https://github.com/nimrod-code/babel>`_.
* Through babel install the `argument_parser module
  <https://github.com/gradha/argument_parser>`_::

    babel install argument_parser

* Finally compile the ``awesome_rmdir`` command::

    nimrod c -d:release awesome_rmdir.nim

* Copy the generated ``awesome_rmdir`` binary to somewhere in your path, or
  create a bash alias for rmdir so it gets run automatically::

    alias rmdir=`/path/to/awesome_rmdir`


Changes
=======

This is version 0.3.1. For a list of changes see the
`docs/CHANGES.rst <docs/CHANGES.rst>`_ file.


Git branches
============

This project uses the `git-flow branching model
<https://github.com/nvie/gitflow>`_. Which means the ``master`` default branch
doesn't *see* much movement, development happens in another branch like
``develop``. Most people will be fine using the ``master`` branch, but if you
want to contribute something please check out first the ``develop`` brach and
do pull requests against that.


Feedback
========

You can send me feedback through `github's issue tracker
<http://github.com/gradha/awesome_rmdir/issues>`_. I also take a look from time
to time to `Nimrod's forums <http://forum.nimrod-lang.org>`_ where you can talk
to other nimrod programmers.
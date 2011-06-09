`ikazuchi.plugins.blockdiag <https://bitbucket.org/t2y/ikazuchi.plugins.blockdiag>`_
is plugin for `ikazuchi <https://bitbucket.org/t2y/ikazuchi>`_ to work with
`blockdiag <http://pypi.python.org/pypi/blockdiag/>`_.

`ikazuchi` is intended to work with other tools since it's a CUI tool.

See the project `documentation <http://t2y.bitbucket.org/ikazuchi/build/html/index.html>`_ for more detail.

Features
========

* Work with **blockdiag** as `ikazuchi` Translator

Setup
=====

by easy_install
----------------

Make environment::

   $ easy_install ikazuchi.plugins.blockdiag

by buildout
-----------

Make environment::

   $ hg clone https://bitbucket.org/t2y/ikazuchi.plugins.blockdiag
   $ cd ikazuchi.plugins.blockdiag
   $ python bootstrap.py -d
   $ bin/buildout


Usage
=====

Show blockdiag's diagram with web browser. For example, use Firefox::

    $ export BROWSER="firefox"  # can set any browser(command)
    $ ikazuchi blockdiag -s "{A -> B;}"

Show blockdiag's diagram from ".diag" file with web browser::

    $ ikazuchi blockdiag -d examples/simple.diag 

Show blockdiag's diagram with Tkinter Editor::

    $ ikazuchi blockdiag -i -d examples/simple.diag 

Show which plugins are available::

    $ ikazuchi -h
    usage: ikazuchi [-h] {rstfile,blockdiag,normal} ...

    positional arguments:
      {rstfile,blockdiag,normal}
                            available plugins. 'normal' means ikazuchi's standard
                            feature so it can be abbreviated

    optional arguments:
      -h, --help            show this help message and exit

Show blockdiag plugin help::

    $ ikazuchi blockdiag -h
    usage: ikazuchi blockdiag [-h] [-a API] [-e ENCODING] [-f LANG] [-q] [-t LANG]
                              [-d DIAG FILE] [-i] [-s SENTENCE] [--version]

    optional arguments:
      -h, --help            show this help message and exit
      -a API, --api API     APIs are ['google', 'microsoft']
      -e ENCODING, --encoding ENCODING
                            input/output encoding
      -f LANG, --from LANG  original language
      -q, --quiet           not to show original sentence to stdout
      -t LANG, --to LANG    target language to translate
      -d DIAG FILE, --diag DIAG FILE
                            target diag file
      -i, --interactive     run with interactive mode
      -s SENTENCE, --sentence SENTENCE
                            target sentence
      --version             show program's version number and exit


Requirements
============

* Python 2.6 or later
* ikazuchi 0.5.2 or later
* blockdiag 0.8.1 or later
* Tkinter
* setuptools or distriubte


License
=======

Apache License 2.0


History
=======

0.1.0 (2011-06-10)
------------------
* first release


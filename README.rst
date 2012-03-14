Kotti Development Buildout
--------------------------

This buildout uses `mr.developer <https://github.com/fschulze/mr.developer>`_ to pull in development versions of `Kotti <https://github.com/Pylons/Kotti>`_, `deform <https://github.com/Pylons/deform>`_, deformdemo and deform_bootstrap.

If you have a fork of any of these packages, adjust the URL in the ``[sources]`` section of the ``buildout.cfg``.

Usage
-----

Bootstrap::

    python2.7 bootstrap.py
    bin/buildout

Start Kotti::

    bin/pserve src/Kotti/development.ini

Start deformdemo::

    bin/pserve src/deformdemo/demo.ini

Start deform_bootstrap's demo::

    bin/pserve src/deform_bootstrap/demo.ini


Running Tests
-------------

To run unit tests for XXX::

    bin/py.test src/XXX

See ``bin/py.test --help`` for more options, or check `py.test's documentation <http://pytest.org/latest/contents.html#toc>`_.


Running Selenium Tests
----------------------

``deformdemo`` and ``deform_bootstrap`` contain selenium tests that run against their respective instance. To run them, do this:

In one Terminal window, fire up the selenium server::

    bin/seleniumrc

In another terminal start the demo instance (see above) and in a third window run the actual tests::

    ./bin/py src/deform_bootstrap/deform_bootstrap/demo/test.py
    ./bin/py src/deformdemo/deformdemo/test.py


Troubleshooting
---------------

If you get an error ``TypeError: Can't use implementer with classes.  Use one of the class-declaration functions instead.`` upon startup you might need to update your python to 2.7.2. You can use the Makefile provided at http://is.gd/make_python to build up-to-date versions of python for development purposes. YMMV.

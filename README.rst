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

To run tests for XXX::

    bin/py.test src/XXX

See ``bin/py.test --help`` for more options, or check `py.test's documentation <http://pytest.org/latest/contents.html#toc>`_.

Troubleshooting
---------------

If you get an error ``TypeError: Can't use implementer with classes.  Use one of the class-declaration functions instead.`` upon startup you might need to update your python to 2.7.2. You can try https://gist.github.com/1893409 to build up-to-date versions of python for development purposes. YMMV.

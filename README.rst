Kotti Development Buildout
--------------------------

This buildout uses mr.developer to pull in development versions of Kotti, deform, deformdemo and deform_bootstrap.

If you have a fork of any of these packages, adjust the URL in the ``[sources]`` section.

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

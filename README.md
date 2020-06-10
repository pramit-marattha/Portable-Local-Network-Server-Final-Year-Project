# Setting-up-a-virtual-environment

## What is a virtual environment:


It basically helps encapsulate python executables and packages and allows experimentation.

``virtualenv`` is a tool to create isolated Python environments. Since Python ``3.3``, a subset of it has been
integrated into the standard library under the `venv module <https://docs.python.org/3/library/venv.html>`_. The
``venv`` module does not offer all features of this library, to name just a few more prominent:

- is slower (by not having the ``app-data`` seed method),
- is not as extendable,
- cannot create virtual environments for arbitrarily installed python versions (and automatically discover these),
- is not upgrade-able via `pip <https://pip.pypa.io/en/stable/installing/>`_,
- does not have as rich programmatic API (describe virtual environments without creating them).

The basic problem being addressed is one of dependencies and versions, and indirectly permissions.
Imagine you have an application that needs version ``1`` of ``LibFoo``, but another application requires version
``2``. How can you use both these libraries? If you install everything into your host python (e.g. ``python3.8``)
it's easy to end up in a situation where two packages have conflicting requirements.

Or more generally, what if you want to install an application *and leave it be*? If an application works, any change
in its libraries or the versions of those libraries can break the application. Also, what if you can't install packages
into the global ``site-packages`` directory, due to not having permissions to change the host python environment?

In all these cases, ``virtualenv`` can help you. It creates an environment that has its own installation directories,
that doesn't share libraries with other virtualenv environments (and optionally doesn't access the globally installed
libraries either).

Tutorials links
------------

**Related projects, that build abstractions on top of virtualenv**

* :pypi:`virtualenvwrapper` - a useful set of scripts for creating and deleting virtual environments
* :pypi:`pew` - provides a set of commands to manage multiple virtual environments
  * `Corey Schafer tutorial <https://www.youtube.com/watch?v=N5vscPTWKOk>`

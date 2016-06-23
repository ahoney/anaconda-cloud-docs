=================
Command Reference
=================

#. :ref:`cli-anaconda`
#. :ref:`cli-anaconda-build`
#. `API Reference <https://api.anaconda.org/docs>`_

Anaconda client is the command line interface (CLI) to Anaconda Cloud,
and can be used for logging in, logging out, managing your account,
uploading files, generating access tokens, viewing tokens, and other
tasks as shown by running

anaconda -h

The full command reference is shown below.


.. _cli-anaconda:

anaconda
--------

Anaconda Cloud command line manager

.. command-json-output:: anaconda --json-help

Authentication
~~~~~~~~~~~~~~

auth
^^^^

.. command-json-output:: anaconda auth --json-help

Manage Authentication tokens

See also:

-  :ref:`Using Anaconda Cloud Tokens <using-tokens>`


login
^^^^^

Authenticate a user

.. command-json-output:: anaconda login --json-help

whoami
^^^^^^

Print the information of the current user

.. command-json-output:: anaconda whoami --json-help

Informational
~~~~~~~~~~~~~

show
^^^^

Show information about an object

.. command-json-output:: anaconda show --json-help

Show information about an object

Examples::

    anaconda show continuumio
    anaconda show continuumio/python
    anaconda show continuumio/python/2.7.5
    anaconda show sean/meta/1.2.0/meta.tar.gz

search
^^^^^^

Search Anaconda Cloud

.. command-json-output:: anaconda search --json-help

Search Anaconda Cloud for packages

config
^^^^^^

Binstar configuration

.. command-json-output:: anaconda config --json-help

anaconda-client configuration

Get, Set, Remove or Show the anaconda-client configuration.

anaconda-client sites


anaconda-client sites are a mechanism to allow users to quickly switch
between Anaconda Cloud instances. This is primarily used for testing the
anaconda alpha site. But also has applications for the on-site `Anaconda
Enterprise <http://continuum.io/anaconda-server>`__.

anaconda-client comes with two pre-configured sites ``alpha`` and
``binstar`` you may use these in one of two ways:

-  Invoke the anaconda command with the ``-s/--site`` option like this to use
   the alpha testing site::

       anaconda -s alpha whoami

-  Set a site as the default::

       anaconda config --set default_site alpha
       anaconda whoami

Add a anaconda-client site


After installing `Anaconda
Enterprise <http://continuum.io/anaconda-server>`__ you can add a site
named **site\_name** like this::

    anaconda config --set sites.site_name.url "http://<anaconda-enterprise-ip>:<port>/api"
    anaconda config --set default_site site_name

Site Options VS Global Options


All options can be set as global options - affecting all sites, or site
options - affecting only one site

By default options are set globally like this::

    anaconda config --set OPTION VALUE

If you want the option to be limited to a single site, prefix the option
with ``sites.site_name`` like this::

    anaconda config --set sites.site_name.OPTION VALUE

Common anaconda-client configuration options


-  ``url``: Set the anaconda api url (default: https://api.anaconda.org)
-  ``verify_ssl``: Perform ssl validation on the https requests.
   verify\_ssl may be ``True``, ``False`` or a path to a root CA pem
   file.

Toggle auto\_register when doing anaconda upload


The default is yes, automatically create a new package when uploading.
If no, then an upload will fail if the package name does not already
exist on the server.

::

    anaconda config --set auto_register yes|no

Managing Packages
~~~~~~~~~~~~~~~~~

package
^^^^^^^

Anaconda Cloud package utilities

.. command-json-output:: anaconda package --json-help


.. _cli-upload:

upload
^^^^^^

Upload packages to Anaconda Cloud

.. command-json-output:: anaconda upload --json-help

::

    anaconda upload CONDA_PACKAGE_1.bz2
    anaconda upload notebook.ipynb
    anaconda upload environment.yml

See Also
''''''''

-  :ref:`Uploading a Conda Package <uploading-conda-packages>`
-  :ref:`Uploading a PyPI Package <uploading-pypi-packages>`


label
^^^^^

Manage your Anaconda Cloud channels

.. command-json-output:: anaconda label --json-help

copy
^^^^

Copy packages from one account to another

.. command-json-output:: anaconda copy --json-help


.. _cli-anaconda-build:

anaconda build
--------------

Anaconda build client for continuous integration, testing and building packages

.. command-json-output:: anaconda-build --json-help

Anaconda Build command

To get started with anaconda build run::

    anaconda build init  anaconda build submit .

See also:

-  :doc:`build`

.. _submitting-builds:

Submitting Builds
~~~~~~~~~~~~~~~~~

.. _cli-submit:

submit
^^^^^^

Submit a directory or github repo for building

.. command-json-output:: anaconda-build submit --json-help


Build command

Submit a build from your local path or via a git url:

See also:

-  :ref:`submit-a-build`
-  :ref:`Submit A Build From Github <github-builds>`


.. _cli-save:

save
^^^^

Save build info to be triggered later

.. command-json-output:: anaconda-build save --json-help


Save build info to be triggered later

See also:

-  :ref:`save-and-trigger-builds`


.. _cli-trigger:

trigger
^^^^^^^

Trigger a build that has been saved

.. command-json-output:: anaconda-build trigger --json-help


Trigger a build that has been saved

See also:

-  :ref:`save-and-trigger-builds`

Hosting Build machines
~~~~~~~~~~~~~~~~~~~~~~

.. _cli-queue:

queue
^^^^^

Build Queue

.. command-json-output:: anaconda-build queue --json-help


worker
^^^^^^

.. command-json-output:: anaconda-build worker --json-help

docker-worker
^^^^^^

.. command-json-output:: anaconda-build docker-worker --json-help

Anaconda Build command

To get started with anaconda worker run::

    anaconda worker register USER/QUEUE -n NAME  anaconda worker run NAME

See also:

-  :ref:`Anaconda Build <build-workers>`

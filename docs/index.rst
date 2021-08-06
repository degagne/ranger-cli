=========
RangerCLI
=========

.. raw:: html

   <hr>

The RangerCLI (command-line interface) provides a straghtforward interface for managing resources within the
Apache Ranger framework. The open-source project is hosted on `GitHub <https://github.com/degagne/ranger-cli>`_
and is buitl on top of the Apache Ranger public REST APIs. 

Installation
============

Before installing the RangerCLI, the following requirements must be met.

* `Python 3.6 <https://www.python.org/downloads/release/python-360/>`_

Furthermore, the following Python libraries are also required and will be installed with the Ranger CLI.

* `click <https://pypi.org/project/click/>`_
* `six <https://pypi.org/project/six/>`_
* `confuse <https://pypi.org/project/confuse/>`_
* `PyYAML <https://pypi.org/project/PyYAML/>`_
* `requests <https://pypi.org/project/requests/>`_
* `urllib3 <https://pypi.org/project/urllib3/>`_
* `xmltodict <https://pypi.org/project/xmltodict/>`_
* `simplejson <https://pypi.org/project/simplejson/>`_

Using the appropriate version of ``pip`` for your Python installation, invoke the following command to install the RangerCLI:

.. code-block:: bash
    :caption: Bash

    $ pip install ranger-cli

You can upgrade the RangerCLI with:

.. code-block:: bash
    :caption: Bash

    $ pip install ranger-cli --upgrade

Once you've installed or updated the RangerCLI, you can verify the installation with:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli --version

Ranger connection profiles
==========================

The RangerCLI supports multiple Apache Ranger connection profiles. These profiles are stored locally ``~/.config/ranger/config.yaml``
and are used to make API calls to multiple Apache Ranger environments.

To create a new profile, invoke the following command:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli configure --policy <profile-name>

.. important::

    If the profile name already exists in the configuration file, it will be overwritten 
    with the new properties.

Example configuration file:

.. code-block:: YAML
    :caption: YAML
    :linenos:

    default:
      endpoint: https://ranger1.example.com:6182
      authentication:
        - jsmith
        - supersecurepassword
      verification: /home/jsmith/.config/ranger/ca-bundle.crt

To use the connection profile

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy --policy <profile-name>

If ``--profile`` option is not invoked, the default profile is used. If the default profile 
is not found, the first profile in the configuration file is used.

Getting Started
===============

To start using the RangerCLI, use the ``--help`` option to view the latest available group commands.

.. code-block:: bash
    :caption: Bash

    $ ranger-cli --help

To view the latest available sub-commands, the ``--help`` option can be used on the group command:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli <group> --help

.. toctree::
    :maxdepth: 2
    :caption: Overview

    overview.rst

.. toctree::
    :maxdepth: 1
    :caption: CLI commands

    /cli/configure.rst
    /cli/policy.rst
    /cli/service.rst
    /cli/servicedef.rst
    /cli/plugins.rst

.. toctree::
    :maxdepth: 2
    :caption: Plugin Templates

    templates.rst

.. toctree::
    :hidden:
    :titlesonly:
    :caption: License

    license.rst

Links
=====

* `Apache Ranger REST APIs <https://ranger.apache.org/apidocs/index.html>`_

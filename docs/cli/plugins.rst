===========
Plugins CLI
===========

Administration for Apache Ranger's plugins public REST API. Users can view Apache Ranger plugins.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins --help

.. contents:: Command examples
    :local:
    :depth: 2
    :backlinks: none

.. raw:: html

   <hr>

Get plugins info
****************

Gets all Apache Ranger plugins info.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --help

Get plugins info by apptype
***************************

Gets all Apache Ranger plugins info by app type.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --apptype yarn

On success, this command returns a JSON object with the service definitions found.

Get plugins info by hostname
****************************

Gets all Apache Ranger plugins info by hostname.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --hostname nn.example.com

On success, this command returns a JSON object with the service definitions found.

Get plugins info by service name
********************************

Gets all Apache Ranger plugins info by service repository name.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli plugins info --service-name cl1_hive

On success, this command returns a JSON object with the service definitions found.
==============
ServiceDef CLI
==============

Administration for Apache Ranger's servicedef service REST API. Users can view,
create, update or delete Apache Ranger service definitions. Service definitions
are use to create service repositories and users must be aware of certain
requirements within the definitions.

Service Definition configurations
=================================

The service definitions contains

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef --help

.. contents:: Command examples
    :local:
    :depth: 2
    :backlinks: none

.. raw:: html

   <hr>

Get service definitions
***********************

Gets service definition data for all Apache Ranger service definitions.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef get

On success, this command returns a JSON object with the service definitions found.

.. note::

    To view the latest service types available, please use ``--help`` option.

Get service definitions by type
*******************************

Gets service definition data for all Apache Ranger service definitions by type.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef get --service-type HDFS

On success, this command returns a JSON object with the service definitions found.

List configuration properties
*****************************

Gets service definition configuration properties which are used to create new service 
repository (or repositories).

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef list-configs --help

Below is an example of listing service definition configuration properties for the Hive service.

.. code-block:: bash
    :caption: Bash

    $ ranger-cli servicedef list-configs --service-type HIVE

.. code-block:: bash
    :caption: Console

                   HIVE Plugin Configs                
    ┏━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
    ┃ PROPERTY     ┃ VALUE                           ┃
    ┡━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┩
    │ name         │ username                        │
    │ mandatory    │ True                            │
    │              │                                 │
    ├──────────────┼─────────────────────────────────┤
    │ name         │ password                        │
    │ mandatory    │ True                            │
    │              │                                 │
    ├──────────────┼─────────────────────────────────┤
    │ name         │ jdbc.driverClassName            │
    │ mandatory    │ True                            │
    │ defaultValue │ org.apache.hive.jdbc.HiveDriver │
    │              │                                 │
    ├──────────────┼─────────────────────────────────┤
    │ name         │ jdbc.url                        │
    │ mandatory    │ True                            │
    │ defaultValue │                                 │
    │              │                                 │
    ├──────────────┼─────────────────────────────────┤
    │ name         │ commonNameForCertificate        │
    │ mandatory    │ False                           │
    │              │                                 │
    └──────────────┴─────────────────────────────────┘

The table above provides the configuration properties required to be included in 
your ``<service>-service.json`` file. 

.. seealso::

    For available templates, please check out :ref:`plugin-templates`

List resource properties
************************

Returns a table with the name, type and default value of the service definition configuration 
properties. These properties are used to create new service repositories.

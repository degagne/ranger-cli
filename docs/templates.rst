.. _plugin-templates:

================
Plugin Templates
================

Plugin templates are used to create or update service repositories. These templates can be
edited then invoked with either:

.. warning::

  This interface is still a "work-in-progess".

Create service repository

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service create --config <service-name>-service.json

Update existing service repository

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service update --config <service-name>-service.json --service-id 12345

HDFS
====

HDFS service JSON template file.

.. literalinclude:: /templates/hdfs-service.json
  :language: JSON
  :caption: hdfs-service.json

Hive
====

Hive service JSON template file.

.. literalinclude:: /templates/hive-service.json
  :language: JSON
  :caption: hive-service.json
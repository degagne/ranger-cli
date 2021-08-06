.. _service-cli:

===========
Service CLI
===========

Administration for Apache Ranger's policy service REST API. Users can view, create, 
update or delete Apache Ranger service repositories.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service --help

.. contents:: Command examples
    :local:
    :depth: 2
    :backlinks: none

.. raw:: html

   <hr>

Get service repository by id
****************************

Gets repository data for an Apache Ranger service repository using the service id.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service get --service-id 1234567

On success, this command returns a JSON object with the service repository found.

Get service repository by name
******************************

Gets repository data for an Apache Ranger service repository using the service name.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli service get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service get --service-name 'HDFS repository'

On success, this command returns a JSON object with the service repository found.

Get all service repositories
****************************

Gets all repository data for every Apache Ranger service repositories.

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli service get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service get

On success, this command returns a JSON object with the service repository (or repositories) found.

Create a service repository
***************************

Creates a new Apache Ranger service repository.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service create --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service create --config hive-service.json

On success, this command returns a JSON object with the service repository created.

.. seealso::

    For additional details on JSON configuration files, please see :ref:`plugin-templates`

Update an existing service repository
*************************************

Updates an existing Apache Ranger service repository.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service update --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service update --service-id 12345 --config hive-service.json

On success, this command returns a JSON object with the service repository updated.

.. seealso::

    For additional details on JSON configuration files, please see :ref:`plugin-templates`

Delete an existing service repository
*************************************

Deletes an existing Apache Ranger service repository.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service delete --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli service delete --service-id 12345

On success, this command returns nothing, otherwise HTTP status code/reason

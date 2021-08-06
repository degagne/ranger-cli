.. _policy-cli:

==========
Policy CLI
==========

Administration for Apache Ranger's policy public REST API. Users can view, create, 
update or delete Apache Ranger policies.

.. note::

    Supports resource-based policies **ONLY**.

    **Resource-based policy**: grants permissions to users and/or groups on a set of resource objects.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy --help

.. contents:: Command examples
    :local:
    :depth: 2
    :backlinks: none

.. raw:: html

   <hr>

.. _policy-id:

Get resource-based policy by id
*******************************

Gets policy data for an Apache Ranger resource-based policy using the policy id.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy get --policy-id 1234567

On success, this command returns a JSON object with the resource-based policy found.

.. _policy-name:

Get resource-based policy by name
*********************************

Gets policy data for an Apache Ranger resource-based policy using the policy name.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli policy get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy get --policy-name 'Demo resource-based HDFS policy'

On success, this command returns a JSON object with the resource-based policy found.

.. _policy-service-name:

Get resource-based policy by service name
*****************************************

Gets policy data for Apache Ranger resource-based policy (or policies) using the 
service repository name.

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli policy get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy get --service-name 'hadoop.example.com_hadoop'

On success, this command returns a JSON object with the resource-based policy found.

.. _policies-all:

Get all resource-based policies
*******************************

Gets all policy data for every Apache Ranger resource-based policies.

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli policy get --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy get

On success, this command returns a JSON object with the resource-based policy (or policies) found.

.. _create-policy:

Create a resource-based policy
******************************

Creates a new Apache Ranger resource-based policy.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli policy create --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy create --config /home/jsmith/hive-policy.json

On success, this command returns a JSON object with the resource-based policy created.

.. _update-policy:

Update an existing resource-based policy
****************************************

Updates an existing Apache Ranger resource-based policy.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy update --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy update --policy-id 12345 --config /home/jsmith/hive-policy.json

On success, this command returns a JSON object with the resource-based policy updated.

.. _delete-policy:

Delete an existing resource-based policy
****************************************

Deletes an existing Apache Ranger resource-based policy.

To display usage documentation, run:

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy delete --help

.. code-block:: bash
    :caption: Bash

    $ ranger-cli policy delete --policy-id 12345

On success, this command returns nothing, otherwise HTTP status code/reason

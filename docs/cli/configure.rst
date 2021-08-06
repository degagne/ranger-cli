=============
Configure CLI
=============

The purpose of the ``configure`` command, is to provide users the ability to create, update or 
delete connection profiles. Connection profiles are use to establish connections to Apache 
Ranger REST API environments.

To display the usage documentation, run: 

.. code-block:: bash
    :caption: Bash
    
    $ ranger-cli configure --help

.. contents:: Command examples
    :local:
    :depth: 2
    :backlinks: none

.. raw:: html

   <hr>

Create a connection profile
***************************

The following command will create the "default" profile. If you wish to create a different 
profile, then you need to include the ``--profile`` option.

.. code-block:: bash
    :caption: Bash

    $ ranger-cli configure

Delete a connection profile
***************************

To delete a connection profile, execute the ``configure`` with the ``--delete`` flag.

.. code-block:: bash
    :caption: Bash

    $ ranger-cli configure --delete --profile <profile-name>

.. warning::

    Please be advised that if you do not include ``--policy`` option, the default profile 
    will be deleted if it exists.
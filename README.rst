.. |backend_master_build| image:: https://circleci.com/gh/ippolab/athena-backend/tree/master.svg?style=svg
    :target: https://circleci.com/gh/ippolab/athena-backend/tree/master

.. |backend_dev_build| image:: https://circleci.com/gh/ippolab/athena-backend/tree/dev.svg?style=svg
    :target: https://circleci.com/gh/ippolab/athena-backend/tree/dev

.. |frontend_master_build| image:: https://circleci.com/gh/ippolab/athena-frontend/tree/master.svg?style=svg
    :target: https://circleci.com/gh/ippolab/athena-frontend/tree/master

.. |frontend_dev_build| image:: https://circleci.com/gh/ippolab/athena-frontend/tree/dev.svg?style=svg
    :target: https://circleci.com/gh/ippolab/athena-frontend/tree/dev

.. _traefik: https://traefik.io/
.. _here: https://docs.traefik.io/user-guide/docker-and-lets-encrypt/
.. _frontend: https://github.com/ippolab/athena-frontend/
.. _api: https://github.com/ippolab/athena-backend/

Build status
------------

Backend
~~~~~~~

+------------+------------------------+
|   BRANCH   | BUILD STATUS           |
+============+========================+
| master     | |backend_master_build| |
+------------+------------------------+
| dev        | |backend_dev_build|    |
+------------+------------------------+

Frontend
~~~~~~~~

+------------+-------------------------+
|   BRANCH   | BUILD STATUS            |
+============+=========================+
| master     | |frontend_master_build| |
+------------+-------------------------+
| dev        | |frontend_dev_build|    |
+------------+-------------------------+

Deploy
------

To deploy Athena you may need installed traefik_ configured for listening docker events or some other proxy. More info about traeifik here_. Then rename ``.env.example`` and change values in file. And last step - set up host name for frontend_ and api_ and start services:

.. code-block:: bash

    export HOSTNAME=example.com
    docker-compose up -d

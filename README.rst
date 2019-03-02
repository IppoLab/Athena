.. |backend_master_build| image:: https://circleci.com/gh/IppoLab/Athena-backend/tree/master.svg?style=svg
    :target: https://circleci.com/gh/IppoLab/Athena-backend/tree/master

.. |backend_dev_build| image:: https://circleci.com/gh/IppoLab/Athena-backend/tree/dev.svg?style=svg
    :target: https://circleci.com/gh/IppoLab/Athena-backend/tree/dev

.. |frontend_master_build| image:: https://circleci.com/gh/IppoLab/Athena-frontend/tree/master.svg?style=svg
    :target: https://circleci.com/gh/IppoLab/Athena-frontend/tree/master

.. |frontend_dev_build| image:: https://circleci.com/gh/IppoLab/Athena-frontend/tree/dev.svg?style=svg
    :target: https://circleci.com/gh/IppoLab/Athena-frontend/tree/dev

.. _traefik: https://traefik.io/
.. _here: https://docs.traefik.io/user-guide/docker-and-lets-encrypt/
.. _frontend: https://github.com/IppoLab/Athena-frontend/
.. _api: https://github.com/IppoLab/Athena-backend/

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

To deploy Athena you need installed traefik_ configured for listening docker events. More info here_. Then rename ``.env.example`` and change values in file. And last step - set up host names for frontend_ and api_ and start services:

.. code-block:: bash

    export ATHENA_FRONT_HOST=athena.example.edu
    export ATHENA_API_HOST=api.athena.example.edu
    docker-compose up -d
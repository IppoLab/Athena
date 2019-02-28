.. _traefik: https://traefik.io/
.. _here: https://docs.traefik.io/user-guide/docker-and-lets-encrypt/
.. _frontend: https://github.com/IppoLab/Athena-frontend/
.. _api: https://github.com/IppoLab/Athena-backend/

Deploy
------

To deploy Athena you need installed traefik_ configured for listening docker events. More info here_. Then rename ``.env.example`` and change values in file. And last step - set up host names for frontend_ and api_ and start services:

.. code-block:: bash

    export ATHENA_FRONT_HOST=athena.example.edu
    export ATHENA_API_HOST=api.athena.example.edu
    docker-compose up -d
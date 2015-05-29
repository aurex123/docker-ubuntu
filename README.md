docker-ubuntu
==================

Base Docker Image con ubuntu trusty.
Contiene las configuraciones básicas como Zona horaria, Locales, etc...


Uso
-----

Para correr esta imagen primero se tiene que generar, ejecuta lo siguiente en esta carpeta:

    docker build -t aurex/ubuntu .

Y para iniciar en modo interactivo, ejecutar:

    docker run --rm -ti --name bash_ubuntu aurex/ubuntu /bin/bash

Extender imagen
-------------------------------
Crea un nuevo `Dockerfile` con el siguiente contenido:

    FROM aurex/ubuntu
    ...
    #Demas Instrucciones
    ...

Despues de eso, genera el nuevo `Dockerfile`:

    docker build -t username/my-image

Y pruebalo:

    docker run -d -P username/my-image

That's it!

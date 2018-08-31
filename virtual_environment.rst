Entorno Virtual
---------------

¿Ha alguna vez escuchado de ``virtualenv``? Si usted es un principiante,
posiblemente no ha escuchado acerca de esto, pero si usted es un
experimentado programador entonces esto bien puede ser una parte vital
de su conjunto de herramientas. 

Así, ¿qué es ``virtualenv``? ``Virtualenv`` es una herramienta la cual nos
permite hacer entornos aislados de python. Imagine que tiene una aplicación
que necesita la versión 2 de una librería, pero otra aplicación requiere la
versión 3. ¿Cómo puede usted usar y desarrollar ambas aplicaciones?

Si usted instala todo dentro de ``/usr/lib/python2.7/site-packages`` (o
donde quiera que se encuentre ubicada su plataforma estándar), es fácil de
finalizar en una situación donde se actualice sin intención un paquete.

En otro caso, imagine que tiene una aplicación la cual está completamente
desarrollada y no quiere hacer ningún cambio a las librerías que esta
utilizando, pero al mismo tiempo comienza a desarrollar otra aplicación
la cual requiere las versiones actualizadas de esas librerías.

¿Qué hará? ¡Utilice ``virtualenv``! Esto crea entornos aislados para su
aplicación de python y le permite instalar librerías de Python en ese
entorno aislado en lugar de instalarlas globalmente.

Para instalarlo, solo digite este comando en el terminal:

.. code:: python

    $ pip install virtualenv

Los comandos más importantes son:

-  ``$ virtualenv myproject``
-  ``$ source myproject/bin/activate``

El primero crea un ``virtualenv`` entorno aislado en la carpeta ``myproject``
y el segundo comando activa ese entorno aislado.

Mientras se crea el ``virtualenv`` usted tiene que tomar una decisión. ¿Quiere que este
``virtualenv`` use paquetes de su sistema ``site-packages`` o instalarlos localmente en
``site-packages`` de su entorno virtual? Por defecto, ``virtualenv`` no dará acceso al 
sitio de paquetes global ``site-packages``.

Si quiere que su ``virtualenv`` tenga acceso a su sistema ``site-packages``, use en cambio 
``--system-site-packages`` cuando lo esté creando de esta forma:

.. code:: python

    $ virtualenv --system-site-packages mycoolproject

Usted puede apagar el ``env`` digitando:

.. code:: python

    $ deactivate

Ejecutando ``python`` después de la desactivación utilizara la versión de python que
tenga por defecto en su sistema.

**Extra**

Puede usar ``smartcd`` es una librería para ``bash`` y ``zsh`` que le permite alternar
su entorno ``bash`` (o ``zsh``) cuando cambia de directorio ``cd``. Esto puede ser
realmente una ayuda para activar o desactivar un ``virtualenv`` cuando usted cambie
directorios. Lo he usado bastante y me encanta. Usted puede leer más acerca de esto
en `GitHub <https://github.com/cxreg/smartcd>`__

Esto fue solo una breve introducción a ``virtualenv``. hay mucha más información sobre
este tema en este `enlace <http://docs.python-guide.org/en/latest/dev/virtualenvs/>`__.

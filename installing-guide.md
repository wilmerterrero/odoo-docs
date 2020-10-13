## COMO INSTALAR ODOO

### REQUERIMIENTOS
1. Equipo con SO Ubuntu 18,04
2. 8GB RAM - Disco SSD
3. IDE (Pycharm)
4. Odoo v13.0 o v14.0

#### GUIA DE INSTALACION
- Instalar todas las dependencias y crear las carpetas correspondientes mediante el instalador ``odoo14.sh``. Descargar [aquí](https://github.com/wilmerterrero/wilmer-odoo).
    - Despues de descargar el archivo. Ir a ``properties`` y habilitar la opcion ``Allow executing file as program``.
    - En la terminal, permitir la escritura y modificacion de los archivos con el comando ``chmod +x odoo14.sh``.
    - Ir a la terminal (``ctrl + shift + t``) y instalar el archivo ``odoo14.sh`` mediante el comando ``./odoo14.sh``.

- Descargar PyCharm 2020 Professional Edition y colocar el proyecto en PyCharm. Solo la carpeta ``odoo``.
    - ##### Espacio de Desarrollo en PyCharm
        - Instalar los ``odoo snippets`` mediante este [link](https://raw.githubusercontent.com/mohamedmagdy/odoo-pycharm-templates/master/Odoo.xml).
            - Crear una carpeta llamada ``templates`` en la ruta de configuracion de PyCharm. Para acceder a ellas vamos a ``Home`` luego teclamos ``ctrl + h`` para mostrar los archivos ocultos. Abrimos la carpeta ``.config``. Buscamos la carpeta de ``JetBrains`` y abrimos la carpeta de PyCharm en donde posteriormente crearemos nuestra carpeta ``templates`` donde pondremos nuestro archivo ``Odoo.xml`` que contiene todos los ``odoo snippets``.
        - ##### Linkeando odoo.conf y la carpeta extra-addons con nuestro proyecto
            - Este archivo contiene toda la informacion de nuestro Odoo. Es **importante**. En el podemos poner la informacion de nuestro odoo. 
            - Para linkear nuestro proyecto odoo en PyCharm solo basta con abrir la terminal y escribir: ``ln -s ../extra-addons`` y luego ``ln -s ../odoo.conf``
        - ##### Preparando el venv
            - Todas nuestras dependencias estaran instaladas, pero necesitamos poner el ``odoo-bin`` como ejecutable de nuestro proyecto. Para eso le damos click a este boton:
            ![venv config](/img/odoo-bin.png)
            - El archivo que sera nuestro ejecutable sera ``odoo-bin`` y le podemos poner cualquier nombre al ejecutable.
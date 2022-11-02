# RIPuppet
A node js library for GUI Ripping on web applications

## Configuración
El archivo `config.json`. El parámetro url indica la dirección de la página web que se va a probar. El parámetro headless es un booleano que indica si el navegador se va a ejecutar en modo headless (sin interfaz gráfica). El parámetro depthLevels indica qué tantos niveles de profundidad debe tener el árbol generado a partir de las interacciones posibles en la interfaz gráfica. El parámetro inputValues es un booleano que indica si se deben utilizar credenciales o los valores del parámetro values. Los parámetros al interior del parámetro values son utilizados para introducir valores específicos a campos del sitio web: en este caso, la llave corresponde al id del elemento en el DOM y el valor corresponde a la cadena de texto que se introducirá en el campo con dicho id. Finalmente, el parámetro browsers indica en qué navegadores se quiere probar la página y puede tomar los valores "chromium", "webkit" o "firefox".

## Instalación
Para ejecutar la prueba debe abrir una terminal y ubicarse en el directorio raíz del repositorio. Desde allí, deberá descargar las dependencias del proyecto ejecutando el comando:

- `npm install` Esto instalará un directorio llamado "node_modules", que contiene las librerías que se utilizan como parte del código del proyecto. El comando puede tardar un poco en completarse, dado que instala librerías de gran tamaño.
- `node index.js` Luego de este paso, puede ejecutar su prueba por medio del comando

## Resultados
En primer lugar, podrá ver que la terminal desde la que ejecutó la prueba le brindará una retroalimentación sobre el proceso. Esta retroalimentación es extensiva e incluye el navegador en el que actualmente se está ejecutando la prueba, luego un listado de nodos y enlaces disponibles para cada estado, el stack de los errores que han ocurrido (si los hay) y algunas líneas informativas sobre el estado de la prueba.

Además, podrá ver que en la ruta donde está ubicada el proyecto se creó un directorio con el nombre "results". Al abrirlo, podrá ver un subdirectorio cuyo nombre corresponde a la fecha y hora en la que se obtuvo el reporte de ejecución de la prueba en formato ISO. Cada vez que ejecute una prueba, se creará uno muy similar con esta convención. Dentro de cada uno, podrá ver un subdirectorio para cada uno de los navegadores donde se interactuó con la página web. En estos se encuentran las capturas de pantalla que se tomaron durante la prueba, tres archivos en formato JSON con información de los grafos y un archivo `report.html`.

Para poder ver el contenido del reporte en su navegador web, debe servir los archivos en un puerto. Esto quiere decir, crear un servidor sencillo que aloje los archivos en su máquina local. Este proceso es bastante sencillo y para lograrlo únicamente necesita tener instalado npm en su máquina (como se indicó en la sección de introducción del tutorial).

- `npm install -g http-server` En una terminal, ubíquese en el directorio results. Desde allí, ejecute el siguiente comando para instalar la librería http-server de Node.js:
- `http-server` Ahora que cuenta con esta herramienta en su computadora, ejecute el siguiente comando para crear un servidor local con los archivos del directorio actual:



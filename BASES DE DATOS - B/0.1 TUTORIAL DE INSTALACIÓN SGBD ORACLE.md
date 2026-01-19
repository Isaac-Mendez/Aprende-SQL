Para hacer la instalación del SGBD Oracle primero tenemos que instalar un software de Java. En este tema primero veremos cómo se instala la JDK y después el cliente y el servidor de Oracle.

## 8.1. Instalación del software JDK

Como el SGBD de Oracle está desarrollado sobre la plataforma Java, es necesario contar con la herramienta que lo ejecuta: la JDK.

Para instalar dicha herramienta se deben seguir los siguientes pasos:

- Acceder a la página web oficial: [https://www.oracle.com/es/](https://www.oracle.com/es/)
- Navegar hasta la sección de JDK
- Descargar la versión correspondiente al sistema operativo (Linux, Windows, macOS)
- Aceptar las condiciones de descarga
- Oracle pedirá una cuenta, por lo que tendrás que crearla
- Tras crear la cuenta, descargar el JDK en el ordenador
- Una vez descargado, comenzar el proceso de instalación
- Durante la instalación se solicitará la ruta de la carpeta
- La instalación avanzará de forma automática
- El programa avisará cuando haya finalizado

## 8.2. Instalación del servidor Oracle Database Express

Una vez que tengamos descargada la JDK, procederemos a descargar e instalar el servidor de la base de datos. En este caso utilizaremos Oracle Database XE, que es la opción gratuita para este sistema operativo. Los pasos para su instalación son los siguientes:

- Acceder a la página de descarga de Oracle Database: [https://www.oracle.com/es/database/technologies/appdev/xe.html](https://www.oracle.com/es/database/technologies/appdev/xe.html)
- Elegir la descarga correspondiente según el sistema operativo.
- Descargar el archivo comprimido en el ordenador.
- Descomprimir el archivo.
- Ejecutar el instalador (Setup) para integrar la configuración en el sistema.
- Seguir el asistente de instalación y aceptar el acuerdo de licencia.
- Introducir un usuario y contraseña (no perder estas credenciales, ya que si se pierden podría ser necesaria una reinstalación del servidor).
- Esperar a que la instalación se complete; esto puede tardar unos minutos.
- Al finalizar, pulsar Finalizar.

Tras este proceso, el servidor quedará instalado.

## 8.3. Instalación del cliente Oracle: SQL Developer

Una vez instalado el servidor, procederemos a instalar el cliente, que deberá conectarse al servidor para ejecutar consultas. El cliente recomendado es Oracle SQL Developer. Recuerde que debe existir una conexión entre el servidor y el cliente.

Pasos para la instalación de Oracle SQL Developer:

- Descargar.
- Desempaquetar
- Descomprimir.
- Ejecutar el programa para su configuración inicial.

Pasos correspondiente:

- Accedemos a la sección de Oracle SQL Developer.
- Seleccionamos la versión para nuestro sistema operativo.
- Al igual que en otras descargas, nos solicita usuario y contraseña.
- Al validar el usuario se descargan los archivos asociados (usuario y contraseña).
- El archivo se descarga en formato comprimido.
- Una vez extraído, nos pedirá la ruta del JDK y allí se instalará SQL Developer.
- Tras la instalación, comprobaremos que funcione correctamente; es recomendable crear un acceso en el escritorio.
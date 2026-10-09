Conceptos Fundamentales: Git, GitHub y Entornos de Python


1. Diferencia entre Git y GitHub
Piensen en Git como el motor que corre en tu propia computadora: es un sistema de control de versiones local que toma "fotografías" (snapshots) del estado de tu código a medida que avanzas, permitiéndote regresar en el tiempo si algo sale mal sin depender de internet.

GitHub, en cambio, es una plataforma en la nube que aloja repositorios de Git. Sirve para almacenar una copia remota de tu proyecto, respaldar tu trabajo, colaborar con otros desarrolladores mediante Pull Requests y mostrar tu portafolio al mundo.


2. ¿Para qué sirve el archivo .gitignore?
El archivo .gitignore es la lista de exclusión de tu proyecto. En él le indicas explícitamente a Git qué archivos o carpetas **debe ignorar por completo** para que nunca entren al control de versiones. 

Se usa para evitar subir archivos temporales del sistema, credenciales o contraseñas secretas (.env), archivos compilados y carpetas pesadas que no forman parte del código fuente real.

3. ¿Por qué .venv no debe almacenarse en GitHub?
La carpeta .venv es el entorno virtual donde se instalan las librerías de Python. No se debe subir por dos razones principales:

ependencia del sistema operativo:Contiene binarios y rutas instaladas específicamente para tu computadora y tu sistema operativo (Windows, macOS o Linux). Si otra persona la descarga, no le funcionará.
Peso innecesario:Puede pesar cientos de megabytes. Subirla satura el repositorio y vuelve lentas las operaciones de descarga y clonación.

4. ¿Para qué sirve requirements.txt?
Ya que no subimos la carpeta .venv, el archivo requirements.txt actúa como la "receta" del proyecto. Es un texto plano que solo contiene la lista con los nombres y versiones exactas de los paquetes requeridos

Cuando alguien clona tu proyecto, solo ejecuta el comando pip install -r requirements.txt dentro de su propio entorno virtual para reconstruir exactamente las mismas dependencias en segundos.

5. Diferencia entre Stage, Commit y Push
El flujo de trabajo en Git sigue tres pasos progresivos:

1.Stage :Es la zona de preparación. Cuando usas git add, estás seleccionando los cambios específicos que quieres incluir en la próxima foto.
2.Commit:Es tomar la foto y guardarla localmente en el historial de tu máquina mediante git commit -m "mensaje". Cada commit tiene un identificador único y una nota explicativa de lo que se hizo.
3.Push:Es subir todos los commits que acumulaste localmente hacia el servidor remoto en GitHub usando git push.

6. ¿Por qué un repositorio puede tener varios commits antes de un push?
Porque Git es un sistema distribuido y local. No necesitas estar conectado a internet ni subir cambios a la nube cada vez que terminas una tarea pequeña.

Puedes realizar un commit por cada avance lógico en tu máquina (por ejemplo: un commit para estructurar la base de datos, otro para crear la interfaz y otro para solucionar un error). Una vez que completas un bloque de trabajo funcional o concluyes tu jornada, envías todo el paquete de commits a GitHub de un solo viaje con un "git push"
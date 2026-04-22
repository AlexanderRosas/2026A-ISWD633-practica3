# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado o utilizó otros comandos que no se mencionan al realizar la práctica también se debe documentar.
Antes de la práctica:
Mi conocimiento sobre Docker se limitaba a la ejecución de procesos aislados y funciones limitadas. Entendía que los contenedores eran eficientes para correr aplicaciones, pero existía una duda sobre la gestión de datos: ¿Qué sucede si el contenedor falla o debe actualizarse, o presenta algun cambio a mitad del desarrollo?

Lo más útil fue descubrir el uso de los Bind Mounts, el poder editar código en mi carpeta de Windows (C:\ArielRosas\DockerPractica) y ver los cambios en el navegador al instante sin reconstruir la imagen ahorra muchísimo tiempo. También aclaré la lógica de puertos: usamos el 8081 en el host para "tunelizar" el acceso al puerto 80 interno del contenedor.

El mayor reto fue un error 403 Forbidden con Nginx. Descubrí que al mapear mi carpeta vacía, esta "tapó" el index.html original de la imagen. Lo arreglé simplemente creando un archivo en mi directorio local.

Comandos adicionales utilizados:

  docker ps -a: Para diagnosticar por qué fallaban los contenedores de MySQL por falta de variables.

  docker volume prune: Para limpiar volúmenes huérfanos y no acumular basura en el disco.

  docker inspect: Para validar que las rutas de Windows se mapearon correctamente en el entorno de Docker.

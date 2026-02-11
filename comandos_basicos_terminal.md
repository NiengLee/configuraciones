# CLI linux cheatsheet
Opciones de resumenes rapidos de comandos en terminal de Linux
- [Linux Commands Cheat Sheet](https://www.geeksforgeeks.org/linux-unix/linux-commands-cheat-sheet/)
- [Linux Commands Cheat Sheet](https://linux-commands.labex.io/)

# Comandos generales


| Comando                   | Acción                                                                 | flags comunes                  |
| ------------------------- | ---------------------------------------------------------------------- | ------------------------------ |
| lsb_release               | Muestra información de la distribución Linux (nombre, versión, etc.).  | -a                             |
| whoami                    | Imprime el usuario efectivo actual.                                    |                                |
| clear                     | Limpia la pantalla (tambien con ctrl+L)                                |                                |
| pwd                       | Imprime la ruta absoluta del directorio actual.                        |                                |
| sudo                      | Ejecuta un comando con privilegios de superusuario (root).             | -u<br>-k                       |
| ls                        | Lista archivos y directorios.                                          | -l<br>-a<br>-h                 |
| cd                        | Cambia el directorio de trabajo actual.                                |                                |
| touch                     | Crea archivo vacío o actualiza timestamps (atime/mtime).               | -a<br>-m                       |
| nano                      | Editor de texto en terminal.( ctrl+o para guardar, ctrl+x)             |                                |
| cat                       | Muestra/concatena shown contenido de archivos a stdout.                | -n                             |
| grep                      | Busca patrones (regex/texto) en líneas de archivos o stdin.            | -n<br>-i<br>-r                 |
| find                      | Busca archivos/directorios por nombre/atributos dentro de una ruta.    | -name<br>-type<br>-maxdepth    |
| mkdir                     | Crea directorios.                                                      | -p                             |
| cp                        | Copia archivos/directorios.                                            | -r<br>-a                       |
| mv                        | Mueve o renombra archivos/directorios.                                 | -f<br>-i                       |
| rm                        | Elimina archivos/directorios.                                          | -r<br>-f                       |
| chmod                     | Cambia permisos de archivos/directorios.                               | -R                             |
| chown                     | Cambia propietario y/o grupo de archivos/directorios.                  | -R                             |
| which                     | Muestra la ruta del ejecutable que se ejecutaría según PATH.           | -a                             |
| tar                       | Empaqueta/desempaqueta archivos (a veces con compresión).              | -c<br>-x<br>-f<br>-v<br>-z     |
| ">"                       | Redirecciona stdout a un archivo (sobrescribe).                        | 2> (stderr)<br>2>&1 (combinar) |
| ">>"                      | Redirecciona stdout a un archivo (agrega al final).                    | 2>> (stderr)2>&1 (combinar)    |
| \|                        | Pipe: pasa stdout del comando izquierdo a stdin del derecho.           |                                |
| &&                        | Ejecuta el siguiente comando solo si el anterior terminó exitosamente. |                                |
| wget                      | Descarga archivos desde una URL.                                       | -O <br>-c                      |
| curl                      | Transfiere datos desde/hacia una URL (HTTP, etc.).                     | -L<br>-o<br>-I                 |
| dpkg                      | Administra paquetes .deb (instalar, listar, consultar).                | -i<br>-l<br>-s                 |


### stdin (standard input)
Flujo de entrada estándar. Es el canal por el cual un programa recibe datos. Por defecto, proviene del teclado, pero puede redirigirse desde un archivo o desde la salida de otro comando mediante tuberías.

### stdout (standard output)
Flujo de salida estándar. Es el canal donde un programa envía su salida normal o resultados. Por defecto, se muestra en la terminal, pero puede redirigirse a un archivo o a otro proceso.

### stderr (standard error)
Flujo de error estándar. Es el canal donde un programa envía mensajes de error o diagnóstico. Es independiente de stdout, lo que permite redirigir errores y salida normal por separado.

# Ejecucion script.sh

# Cronjob ejecucion de Tareas promgramadas
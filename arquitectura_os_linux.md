Referencia: [ByteByteCode](https://blog.bytebytego.com/p/ep63-linux-file-system-explained)


| carpeta                           | descripcion                                                                                                                                     | Modificable |
| --------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| /bin                              | Ejecutables esenciales para arrancar y operar en modo rescate (p. ej., sh, ls, cp).                                                             | ❎           |
| /bin.*.usr-is-merged              | Compatibilidad por “usr merge”: /bin (y similares) apuntan a /usr/bin. Recomendación: no tocar; no crear/borrar manualmente.                    | ❎           |
| /boot                             | Archivos de arranque (kernel, initramfs, bootloader: GRUB).                                                                                     | ❎           |
| /cdrom                            | Punto de montaje tradicional para CD/DVD. Normalmente no se toca.                                                                               | ❎           |
| /dev                              | Dispositivos expuestos como archivos; virtual (udev). Recomendación: no tocar manualmente; solo diagnóstico muy controlado.                     | ❎           |
| /etc                              | Configuración del sistema y servicios (network, ssh, systemd, apt, etc.). Recomendación: tocar parcialmente con cuidado; hacer backups antes.   |             |
| /home                             | Datos y configuración de usuarios. Recomendación: sí se toca; lugar recomendado para trabajo de usuario.                                        |             |
| /lib, /lib64, /lib*.usr-is-merged | Librerías esenciales del sistema y del loader dinámico. Recomendación: no tocar; no borrar/editar a mano.                                       | ❎           |
| /lost+found                       | Recuperación de ext* tras fsck. Recomendación: no tocar salvo inspección post-recuperación y con criterio.                                      | ❎           |
| /media                            | Montajes automáticos de medios removibles. Recomendación: se puede usar/montar; evitar modificar estructura interna manualmente.                |             |
| /mnt                              | Mountpoint temporal para montajes manuales. Recomendación: sí se puede usar; mantener orden.                                                    |             |
| /opt                              | Software “extra”/terceros fuera del gestor de paquetes. Recomendación: sí se toca parcialmente; buen lugar para instalaciones manuales.         |             |
| /proc                             | FS virtual con info del kernel y procesos. Recomendación: no tocar (no crear/borrar); lectura diagnóstico; escritura solo knobs específicos.    | ❎           |
| /root                             | Home de root. Recomendación: tocar solo como administrador; evitar para trabajo normal.                                                         |             |
| /run                              | Datos volátiles de la sesión (PID files, sockets, estado). Recomendación: no tocar; se limpia al reiniciar.                                     | ❎           |
| /sbin y /sbin*.usr-is-merged      | Binarios de administración del sistema; con usr-merge suele apuntar a /usr/sbin. Recomendación: no modificar.                                   | ❎           |
| /snap                             | Datos y montajes de paquetes Snap. Recomendación: no tocar a mano; administrar con comandos snap.                                               | ❎           |
| /srv                              | Datos servidos por servicios (convención). Recomendación: se puede usar si se adopta; no crítico por defecto.                                   |             |
| /sys                              | sysfs virtual (dispositivos, drivers, parámetros). Recomendación: no tocar manualmente; lectura diagnóstico; escritura solo casos específicos.  | ❎           |
| /tmp                              | Temporales; puede limpiarse al reiniciar. Recomendación: se usa, pero no guardar nada importante; borrar con cuidado.                           |             |
| /usr                              | Mayor parte del software del sistema (/usr/bin, /usr/lib, /usr/share). Recomendación: no modificar a mano; gestionar con apt.                   | ❎           |
| /var                              | Datos variables: logs, caches, colas, datos de servicios. Recomendación: tocar parcialmente (revisar/limpiar con criterio); no borrar a ciegas. |             |
| /swap.img                         | Archivo de swap (memoria virtual). Recomendación: no tocar salvo reconfiguración explícita.                                                     | ❎           |

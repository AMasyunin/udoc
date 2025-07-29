# Activación masiva

Si está transfiriendo una gran cantidad de dispositivos GPS de otra plataforma a Navixy, puede ser una tarea desalentadora activar cada dispositivo manualmente. Ahí es donde la activación masiva resulta útil. Con esta función, puede registrar cientos o incluso miles de dispositivos con un solo archivo CSV o Excel. Antes de comenzar, asegúrese de que su archivo CSV contenga las siguientes columnas en el orden especificado:

- user\_id
- model
- label
- device\_id
- phone
- apn\_name
- apn\_user
- apn\_password
- comment

Si los dispositivos deben asignarse a diferentes usuarios, complete la columna `user_id`. En caso de un archivo sin `user_id`, todos los dispositivos se añadirán a un solo usuario. Evite usar caracteres especiales como "+", "°", o dobles espacios en el archivo. El campo de comentario es opcional y puede usarse para añadir información adicional sobre un dispositivo. También proporcionamos un [archivo de ejemplo](https://www.navixy.com/wp-content/uploads/2022/04/hardware-trackers-activation-example.csv) para guiarle con el formato.

Una vez que se haya creado el archivo de carga masiva, comuníquese con el equipo de Soporte de Navixy para recibir asistencia adicional con la carga.

Tenga en cuenta que la cantidad mínima para carga masiva es de 30 dispositivos.

### Activación masiva de la aplicación X-GPS tracker

En el caso de la aplicación móvil X-GPS Tracker, utilice los siguientes nombres de columnas y orden:

- model
- label
- notification\_phone
- notification\_email

Los ID de dispositivo se generarán automáticamente. Siempre estamos listos para ayudarle con cualquier problema relacionado con la activación masiva u otras funciones. Si tiene alguna pregunta o inquietud, no dude en comunicarse con nuestro equipo de éxito del cliente.
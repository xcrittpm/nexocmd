---
layout: page
title: Manual
permalink: /manual
---

## 1. Primeros pasos

1. Abre NexoCMD y pulsa **+** (o ⌘N) para crear una conexión.
2. Elige **SSH** o **RDP**, escribe el servidor (nombre o IP) y, si hace falta, el puerto.
3. En **Autenticación**, indica el usuario y elige **Contraseña** o **Clave privada**.
4. Pulsa **Guardar**. Para conectar, haz doble clic en la conexión (en Mac) o pulsa **Conectar** (⌘↩).

Si no guardas la contraseña, NexoCMD te la pedirá al conectar y podrás guardarla en el llavero en ese momento.

## 2. Primera conexión a un servidor

La primera vez que te conectas a un servidor, NexoCMD te muestra su **huella** (por ejemplo `SHA256:…`). Compárala
con la del servidor (`ssh-keygen -lf /etc/ssh/ssh_host_ed25519_key.pub`) y pulsa **Confiar y conectar**.

Si en otra ocasión la huella **cambia**, verás un aviso en rojo. Puede deberse a una reinstalación del servidor,
pero también a un ataque. No continúes si no esperabas el cambio. Puedes revisar y olvidar servidores en
**Más → Servidores de confianza**.

## 3. Claves SSH

En **Más → Claves SSH** puedes importar una clave desde un archivo o pegarla. Se admiten Ed25519, ECDSA y RSA. Si la
clave tiene frase de paso, puedes guardarla o dejar que NexoCMD te la pida al conectar. Después, en la conexión,
elige **Clave privada** y selecciona la clave.

Las claves se guardan cifradas en el llavero de tu dispositivo y nunca salen de él.

## 4. El terminal

- Al conectar, el terminal ocupa toda la ventana. Cada conexión abierta es una **pestaña** arriba.
- **⇧⌘L** (o el botón de la izquierda de las pestañas) vuelve a la lista de servidores sin cerrar las sesiones.
- **⇧⌘]** y **⇧⌘[** cambian de pestaña; **⇧⌘W** cierra la sesión activa.
- Si la conexión se corta, pulsa **Reconectar** (⌘R). El historial del terminal se conserva.
- En **Ajustes** eliges el tema (Noche, Grafito o Papel) y el tamaño de letra.

## 5. Panel de archivos (SFTP)

A la izquierda del terminal aparece el panel de archivos del servidor. Arrastra su borde para cambiar el ancho, o
pulsa **⇧⌘B** para mostrarlo u ocultarlo. En iPhone se abre como una hoja desde la parte inferior.

- **Seguir al terminal** (icono de cadena): cuando haces `cd` en el terminal, el panel cambia a esa carpeta. Funciona
  con bash y zsh. Para lograrlo, al conectar NexoCMD envía al shell una línea que le pide indicar su carpeta en cada
  prompt y la borra de la pantalla; no modifica ningún archivo del servidor. Puedes desactivarlo en cada conexión.
- **Abrir carpetas**: doble clic (Mac) o toque (iPhone/iPad).
- **Descargar**: doble clic en un archivo o menú contextual → Descargar. En Mac se guarda en la carpeta Descargas; en
  iPhone y iPad eliges dónde guardarlo.
- **Subir**: arrastra archivos desde el Finder al panel, o usa **… → Subir archivos**.
- **Renombrar, eliminar, nueva carpeta, copiar ruta**: menú contextual (clic derecho o pulsación larga).
- Las transferencias aparecen abajo con su progreso y se pueden cancelar.

## 6. Barra de estado del servidor

Debajo del terminal se muestran la CPU, la memoria, el disco, la carga, la red y el tiempo que lleva encendido el
servidor. Se actualiza cada 3 segundos con un comando de solo lectura y no aparece en el terminal. Está disponible en
servidores Linux.

## 7. Organizar tus servidores

- **Carpetas**: botón **+** junto a «Carpetas» en la barra lateral. Mueve conexiones con el menú contextual.
- **Etiquetas**: escríbelas separadas por comas en la conexión; aparecen en la barra lateral.
- **Favoritas** y **Recientes**: accesos rápidos en la barra lateral.
- **Búsqueda**: por nombre, servidor, usuario o etiqueta.

## 8. Copia de seguridad

En **Ajustes → Copia de seguridad** puedes exportar tus conexiones, carpetas y servidores de confianza a un archivo
JSON e importarlo en otro dispositivo. **No incluye contraseñas ni claves**, que debes volver a añadir.

## 9. Escritorio remoto (RDP)

Ya puedes guardar y organizar conexiones RDP (usuario, dominio, resolución, portapapeles). La conexión al escritorio
remoto llegará en una próxima versión.

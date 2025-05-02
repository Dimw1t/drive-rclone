# drive-rclone

![image](/.img/oM4FUca.png)

Repositorio con instrucciones para montar Google Drive en sistemas Linux utilizando `rclone`.

rclone permite montar Google Drive como un sistema de archivos local en tu máquina, lo que te permite interactuar con tus archivos de Drive (leer, escribir, copiar, mover) directamente desde la línea de comandos o aplicaciones, como si fueran archivos locales. También permite sincronizar, hacer copias de seguridad y transferir archivos entre Google Drive y otros servicios en la nube de manera eficiente.

#### Automatico (Opción 1)
`
rclone config create gdrive drive
`
#### Manual (Opción 2)
`
rclone config
`
1. Pulsamos `n`

![image](/.img/1.png)

2. Introduce un nombre para el remote:

![image](/.img/2.png)

3. Selecciona el tipo de servicio que vamos a configurar (En este caso el `18` es google drive):

![image](/.img/3.png)

4. Cuando te pregunte por el `client_id`, déjalo en blanco.. 
5. Igual con el `client_secret`, déjalo vacío también.

![image](/.img/4.png)


7. Elige los permisos que quieres dar al remote:

![image](/.img/5.png)

7. Donde guardar la configuración: pulsa Enter para usar la ruta por defecto..
8. En configuración avanzada, responde con "`n`".

![image](/.img/6.png)

9. Cuando pregunte si deseas usar autoconfiguración, responde "`y`".
10. Se abrirá una ventana del navegador para autenticar tu cuenta de Google. Si no se abre automáticamente, se mostrará una URL para copiar y pegar.
11. Si todo salió bien, verás un mensaje de éxito como este:

![image](/.img/7.png)


### 📁 Crear y montar directorios:
`
mkdir /home/dimw1t/Drive
rclone mount gdrive:google-drive /home/dimw1t/Drive --allow-other --daemon
`
### ✅ Verificación:
`
df
`




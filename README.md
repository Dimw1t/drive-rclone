# drive-rclone

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

![image](https://github.com/user-attachments/assets/a8488a41-2377-4ff3-91a6-ec0061d33e3e)

2. Introduce un nombre para el remote:

![image](https://github.com/user-attachments/assets/70b41722-adaf-4b88-9ebb-980ff4542ef8)

3. Selecciona el tipo de servicio que vamos a configurar (En este caso el `18` es google drive):

![image](https://github.com/user-attachments/assets/8f5782ff-6681-4a09-bd2b-e8bc8cf1a3e0)

4. Cuando te pregunte por el `client_id`, déjalo en blanco.. 
5. Igual con el `client_secret`, déjalo vacío también.

![image](https://github.com/user-attachments/assets/26325672-330f-41c0-90c8-1061d94fad0a)


7. Elige los permisos que quieres dar al remote:

![image](https://github.com/user-attachments/assets/f3692e1c-8854-4db0-b42a-d05fda1538da)

7. Donde guardar la configuración: pulsa Enter para usar la ruta por defecto..
8. En configuración avanzada, responde con "`n`".

![image](https://github.com/user-attachments/assets/01de0930-4f62-4d94-9b27-964be66e7e72)

9. Cuando pregunte si deseas usar autoconfiguración, responde "`y`".
10. Se abrirá una ventana del navegador para autenticar tu cuenta de Google. Si no se abre automáticamente, se mostrará una URL para copiar y pegar.
11. Si todo salió bien, verás un mensaje de éxito como este:

![image](https://github.com/user-attachments/assets/69d0f25b-8d7d-457c-bc3d-b79f6fadd9e7)


### 📁 Crear y montar directorios:
`
mkdir /home/dimw1t/Drive
rclone mount gdrive:google-drive /home/dimw1t/Drive --allow-other --daemon
`
### ✅ Verificación:
`
df
`




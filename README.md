# drive-rclone


## Instalación rclone


#### Instalar

apt update
apt upgrade
apt install rclone


### Configurar (Elige una de las dos opciones)

#### Automatico (Opción 1)

rclone config create gdrive drive

#### Manual (Opción 2)

rclone config

1. Pulsamos n

![image](https://github.com/user-attachments/assets/a8488a41-2377-4ff3-91a6-ec0061d33e3e)

2. Introducimos un nombre:

![image](https://github.com/user-attachments/assets/70b41722-adaf-4b88-9ebb-980ff4542ef8)

3. Seleccionamos el servicio que vamos a configurar (En este caso el 18 es google drive):

![image](https://github.com/user-attachments/assets/8f5782ff-6681-4a09-bd2b-e8bc8cf1a3e0)

4. Nos pide la cuenta de google, pero lo dejamos en blanco. 
5. Nos pide la contraseña, pero lo dejamos en blanco.

![image](https://github.com/user-attachments/assets/26325672-330f-41c0-90c8-1061d94fad0a)


7. Selecionamos los permisos que queremos darle:

![image](https://github.com/user-attachments/assets/f3692e1c-8854-4db0-b42a-d05fda1538da)

7. Donde se va a guardar la configuración, si no ponemos nada se coge por defecto.
8. En editar configuración avanzada, seleccionamos "n".

![image](https://github.com/user-attachments/assets/01de0930-4f62-4d94-9b27-964be66e7e72)

9. Nos pregunta si queremos autoconfigurarlo y seleccionamos "y".
10. Se nos habre una interfaz para poder configurar la cuenta de google, si no se abre directamente en la terminal esta la url:

![image](https://github.com/user-attachments/assets/9b1fa0fa-2986-4a14-bdf4-1a19e14ae5c8)

11. Una vez configurada nos tiene que salir este mensaje:

![image](https://github.com/user-attachments/assets/69d0f25b-8d7d-457c-bc3d-b79f6fadd9e7)


### Configurar directorios:

mkdir /home/dimw1t/Drive
rclone mount gdrive:google-drive /home/dimw1t/Drive --allow-other --daemon

### Comprobar

df





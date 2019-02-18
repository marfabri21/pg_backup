# pg_backup
Script para respaldar base de datos postgres replicacion Tot Standby

Requisitos.

Se requieren que se encuentre instalado en el equipo donde se ejecuta los paquetes:

- pg_dump (Creación del respaldo)
- mailx (Envio de reportes de errores)
- gzip (Compresión del respaldo)

Requiere tener correctamente instalado mailx para el envio de reportes.
Instalación mailx:

yum -y update
yum install -y mailx
We can now start sending e-mails using

create a symbolic link

ln -s /bin/mailx /bin/email
###Set an External SMTP Server to Relay E-Mails

vi /etc/mail.rc
edit

set smtp=smtps://smtp.gmail.com:465
set smtp-auth=login
set smtp-auth-user=USERNAME@YOURDOMAIN.COM
set smtp-auth-password=YOURPASSWORD
set ssl-verify=ignore
set nss-config-dir=/etc/pki/nssdb/
example usage :

echo "Your message" | mail -v -s "Message Subject" email@address

# Instalar-emby-centos7
Como instalar emby en  centos 7

Pasos para la instalacion de un servidor de contenido en Centos 7.

Herramientas:
  Servidor con Centos 7
  
Pasos:
- 1 Instalar wget: yum install wget
- 2 Instalar epel: Escribir en consola yum install epel-release
- 3 Instalar Emby (se uso la version estable):
  - cd /etc/yum.repos.d/
  - wget http://download.opensuse.org/repositories/home:emby/CentOS_7/home:emby.repo
  - yum install emby-server
- 4 Iniciar emby: systemctl start emby-server
- 5 Habilitar los puertos 8096
  - firewall-cmd --zone=public --add-port=8096/tcp
  - firewall-cmd --zone=public --add-port=8096/udp
- 7 Entrar a tu navegador: http://localhost:8096 o http://iplocal:8096
- 8 Agregar contenido y disfrutar.


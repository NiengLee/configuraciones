# Instalación de docker

Primero: descargar el paquete docker del sitio oficial :

 [Instalación de docker](https://docs.docker.com/desktop/setup/install/linux/ubuntu/)

Luego, ir a esta sección y seguir estos pasos:

![[Pasted image 20260210143159.png]]

Pasos de comandos para la instalación de docker : 

```bash
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg lsb-release

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install ./docker-desktop-amd64.deb

systemctl --user start docker-desktop

```

Finalmente ejecutamos los siguiente comandos para verificar instalación : 

```bash
docker --version
docker compose version

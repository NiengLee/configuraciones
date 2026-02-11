# Instalación de vsCode

[Sitio oficial](https://code.visualstudio.com/)

Lista de comandos para la instalación de VsCode:


```bash
sudo apt update && sudo apt install wget gpg software-properties-common apt-transport-https -y

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /usr/share/keyrings/

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list

sudo apt update && sudo apt install code -y

sudo apt install libxss1 libasound2 -y
```

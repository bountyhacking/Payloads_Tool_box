```bash
# Esentials
sudo apt-get update -y && sudo apt-get upgrade -y # Actualizar y upgredear el sistema
setxkbmap [es/eng] # Cambiar el layout en el teclado (Despues de cada reinicio se re-establece por defecto)
sudo apt install htop # Administrador de tareas
sudo apt install gnome-control-center # Para hacer uso de configuraciones
sudo apt install flameshot # Para fotocapturas
sudo apt install speedtest
sudo apt install redshift # Para filtro de luz azul
sudo apt install seclists # Usefull wordlist for pentesting
sudo apt install cmatrix # Animated matrix wallpaper
sudo reboot
sudo poweroff
sudo apt install alien # Conversor de archivos TAR.GZ y RPM a .DEB
# Install docker on linux (debian based)
sudo apt install -y docker.io && sudo apt-install docker-compose
sudo systemctl enable docker --now
docker
# Install postman
# Download .tar.gz file on Postman website 
tar xvzf ~/Downloads/Postman*.tar.gz -C /tmp/
sudo chown -R root:root /tmp/Postman
sudo mv /tmp/Postman /opt/
sudo ln -s /opt/Postman/app/Postman /usr/local/bin/Postman
Postman
apktool # Para pentesting mobile
d2j-dex2jar # Conversor dex to jar files
# Install Nuclei for bug bounty
sudo apt install golang
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
```

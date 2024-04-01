# Anonimato usando Proxy-chains
1. Ejecutar los siguientes comandos:
```bash
sudo apt-get install proxychains
sudo apt-get install tor
nano /etc/proxychains.conf
sudo service tor start
```
2. localizar y luego editar el archivo de configuracion proxychains.
- Debemos comentar todas las configuraciones. Exepto la opcion 'dynamic_chain'
```bash
locate proxychains # Por defecto deberia estar en el endpoint /etc/proxychains.conf
sudo nano /etc/proxychains.conf
```
3. Ejecutar la herramienta:
```bash
# Para ejecutar la herramienta usando firefox
proxychains firefox
# Para ejecutar la herramienta usando firefox dada una URL
proxychains firefox [URL OR ENDPOINT HERE]
#Example
proxychains firefox https://www.youtube.com/watch?v=5EiO1hFRR7o&list=PLHOa2HIo3PL-By4D2E1iUYFnRsGrl3azK
```
4. Opcional, Comprobar que la herramienta funciona correctamente:
```bash
proxychains firefox https://www.youtube.com/watch?v=5EiO1hFRR7o&list=PLHOa2HIo3PL-By4D2E1iUYFnRsGrl3azK
```

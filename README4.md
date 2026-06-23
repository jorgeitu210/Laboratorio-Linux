## Dia 6 Instalar herramientas útiles  
Este dia comenzamos aprendiendo a instalar herramientas utiles dentro del mundode Linux que con el paso nos serviran bastante como Comprobar interfaces, Probar conectividad HTTP, Rastrear ruta, Escaneo rapido de red local y Captura de paquetes  

---

# Instalacion  

````
sudo apt update
sudo apt upgrade -y
sudo apt install -y net-tools curl wget traceroute nmap tcpdump htop vim git  
````
Lo que hacemos aqui es actualizar la lista de paquetes con "sudo apt update" solo descarga la información nueva sobre versiones disponibles  
Despues con "sudo apt upgrade -y" se descarga e instala las actualizaciones disponibles para los paquetes ya instalados  
y por ultimo "sudo apt install -y net-tools curl wget traceroute nmap tcpdump htop vim git" funciona para instalar los paquetes listados, el -y acepta automaticamente cualquier confirmación  

---

# Como usarlos  
````
ip a  
ifconfig  
````
Los dos tienen la misma funcion sin embargo "ip a" se usa o forma parte de la suite moderna iproute2. Muestra todas las interfaces de red de la VM(loopback, adaptador virtual, etc), incluye detalles como la dirección IP, estado de la interfaz y direccion de broadcast  
"ifconfig" pertenece al paquete net-tools mas antiguo, hace lo mismo pero esta en desuso  

---

# Comprobar la conexión

````
curl -I https://google.com
````

Este comando sirve para probar la conexion HTTP con un servidor y obtener unicamente las cabeceras de respuesta (no descargar la pagina)  
"curl" es la herramienta de hacer peticiones web desde la terminal  
"-I" es la opcion que indica solo mostrar cabeceras HTTP"  
"https://google.com" es la URL a la que se conecta  

---

# Rastrear ruta  

````
traceroute google.com
````
Lo que vemos es la ruta que siguen tus paquetes desde tu VM hasta el servidor de Google, y cada linea representa un salto ó hop es decir dispositivo intermedio  
10.0.2.2 seria el salto 1 de tu gateway en VM  
192.250.1.1 el router fisico  
google.com el salto final  

---

# Escaneo de hosts activos en la red local
````
nmap -sn 192.250.1.0/24
````
"nmap" sirve como herramienta de escaneo de redes y puertos  
"-sn" solo detecta si los hosts estan activos, no escanea puertos  
"192.250.1.0/24" es el rango de direcciones IP de tu red local  

---

# Capturar trafico de red en tu interfaz  
````
sudo tcpdump -i enp0s3 -c 50 -w captura.pcap
````
sirve para capturar trafico de red en tu interfaz y guardarlo en un archivo .pcap que luego puedes analizar con herramientas como Wireshark  
"sudo" necesita permisos de administrador para capturar paquetes  
"tcpdump" herrramienta de captura de trafico en tiempo real  
"-i enp0s3" nos indica la interfaz de red a escuchar en la VM es enp0s3  
"-c 50" captura exactamente 50 paquetes  
"-w captura.pcap" guarda la captura en un archivo llamado captura.pcap en lugar de mostrarla en pantalla  
Cuando lo ejecutamos la VM escucha todo el trafico que pasa, se guardan los paquetes que pueden ser pings, HTTP, DNS, etc. y se gurda un archivo captura  

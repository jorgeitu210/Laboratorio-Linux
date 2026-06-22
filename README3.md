# Practica del dia 3
---
## Configurar red en VirtualBox <b> Este dia fue de conocer y configurar la red en VirtualBox:


Abrimos la VB seleccionamos la VM nos vamos a configuracion, Red. <b>
Acivamos el Adaptador 1 en modo NAT (Esto nos permite que la VM use la conexion de nuestro host)

---

## Probar la conexion a Internet

Usamos: <b>
ping -c4.8.8.8.8 <b>
ya que nos permite probar la conexión con el servidor DNS de Google usando la IP.

---

## Probar resolucion de nombres (DNS)

Colocamos en nuestra terminal ping -c 4 google.com <b>
Lo cual prueba que la VM puede resolver nombres de dominio a direcciones IP. (Si funciona, la DNS esta configurada correctamente)

---

## Ver la configuración de red

Tecleamos en la terminal: <b>
ip a <b>
Esto nos muestra tus interfaces de red y direcciones IP


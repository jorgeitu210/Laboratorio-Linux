# 📚 Práctica Linux - Semana 1

En este 4to dia aprendi los **7 pasos básicos en Linux** que realice durante la práctica.

---

## Paso 1: Crear usuario nuevo
```
sudo adduser prueba
```
---

## Paso 2: Cambiar contraseña de usuario
```
sudo passwd prueba
```
---

## Paso 3: Crear archivo y revisar permisos
```
echo "Hola Linux" > demo.txt  
ls -l demo.txt
```

![Captura Paso 4](Captura%20de%20pantalla%202026-06-21%20180427.png)
---

## Paso 4: Cambiar permisos
```
chmod 644 demo.txt  
ls -l demo.txt
```
---

## Paso 5: Cambiar propietario
```
sudo chown prueba demo.txt  
ls -l demo.txt
```
---

## Paso 6: Ver procesos
```
ps aux | head -10 <br> top
```

![Captura Paso 4](Captura%20de%20pantalla%202026-06-21%20180557.png)
---
![Captura Paso 4](Captura%20de%20pantalla%202026-06-21%20180623.png)
---

## Paso 7: Finalizar procesos
pkill nano

---

![Captura Paso 4](Captura%20de%20pantalla%202026-06-21%20180646.png)

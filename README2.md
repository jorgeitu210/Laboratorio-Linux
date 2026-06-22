# 📚 Práctica Linux - Semana 1

En este 4to dia aprendi los **7 pasos básicos en Linux** que realice durante la práctica.

---

## 🔹 Paso 1: Crear archivo
```bash
echo "Hola Linux" > demo.txt
ls -l demo.txt
---
## 🔹 Paso 2: Ver contenido
```bash
cat demo.txt
---
## 🔹 Paso 3: Listar archivo
```bash
ls -l demo.txt
---
## 🔹 Paso 4: Cambiar permisos
```bash
chmod 644 demo.txt
ls -l demo.txt
---
## 🔹Paso 5: Cambiar propietario
```bash
sudo chown prueba demo.txt
ls -l demo.txt
---
## 🔹Paso 6: Ver procesos
```bash
ps aux | head -10
top
---
## 🔹Paso 7: Finalizar procesos
```bash
pkill nano
---
![Captura Paso 4](img/paso4.png)

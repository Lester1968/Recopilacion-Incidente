# 🛡️ Laboratorio: Recopilación de Información del Sistema Después de un Incidente

## 📘 Descripción
Este laboratorio tiene como objetivo guiar al usuario en la recolección de información crítica de un sistema después de un incidente de seguridad. Se exploran comandos esenciales para identificar posibles intrusiones y revisar archivos de registro relevantes.

## 🎯 Objetivos
- Recopilar información volátil y persistente del sistema tras un incidente.
- Analizar registros del sistema que puedan evidenciar accesos no autorizados o fallos de seguridad.

## 🧠 Contexto
Cuando ocurre un incidente de ciberseguridad, es crucial actuar rápidamente para preservar evidencia digital. Esta práctica simula el rol de un analista de respuesta ante incidentes, utilizando herramientas disponibles en un entorno de laboratorio virtualizado con CSE-LABVM.

## 🛠️ Requisitos
- PC con VirtualBox.
- Máquina virtual **CSE-LABVM** correctamente instalada y funcional.

## 🧪 Instrucciones de Laboratorio

### Paso 1: Abrir Terminal en CSE-LABVM
```bash
# Iniciar VM y abrir terminal
```

### Paso 2: Recopilar Información Volátil
Ejecutar los siguientes comandos para capturar el estado del sistema:
```bash
sudo su
echo "Fecha:"; date
uname -a
ifconfig -a
netstat -ano
ps axu
route -n
```
Guardar todo en un archivo:
```bash
# Redirigir la salida a un archivo
[comandos] > report.txt
less report.txt
```

### Paso 3: Analizar Archivos de Registro del Sistema
Revisar los siguientes logs:
```bash
cat /var/log/auth.log | less          # Autenticaciones
last -f /var/log/btmp                 # Intentos fallidos
last -f /var/log/wtmp                 # Sesiones activas
```

## 🧰 Tecnologías Utilizadas
- Linux (dentro de CSE-LABVM)
- Comandos de red y administración del sistema
- Archivos de log en /var/log/

## 🖼️ Capturas de Pantalla
Puedes añadir capturas de terminal, resultados de logs o análisis relevantes en la carpeta `capturas/`.

## 👨‍💻 Autor
**Lester Dávila**  
Proyecto educativo dentro del plan de formación en Ciberseguridad.

## 📄 Licencia
Este proyecto es de uso educativo y no incluye una licencia abierta específica. Para reutilización, contactar con el autor.

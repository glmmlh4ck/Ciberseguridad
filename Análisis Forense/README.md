# ANÁLISIS FORENSE

En esta guía encontraremos todos los usos sobre herramientas de forense.

---

## ÍNDICE:
> | PREVIA |
> |-----------|
1. [Análisis previo](#análisis-previo)
2. [Detección de hashes](#hashes)
> | WINDOWS |
> |-----------|
3. [FTK Imager](#ftk-imager)
> | LINUX |
> |-----------|
4. [LiME](#lime)
5. [Volatility](#volatility)
6. [Volatility Standalone](#standalone)
7. [Autopsy](#autopsy)
> | DESCARGAS |
> |-----------|
8. [Instalación de los programas](#descargas)

<!--------------------------------- ANALISIS PREVIO ----------------------------------------->

---

## ANÁLISIS PREVIO:

> | WINDOWS |
> |-----------|

- Procesos activos:
```markdown
Get-Process
```

- Registros de eventos:
```markdown
Get-EventLog
```

- Historial de comandos:
```markdown
et-Command
```

  
> | LINUX |
> |-----------|

- Procesos activos:
```markdown
ps aux
```
```markdown
ps axjf
```

- Procesos de red escuchando:
```markdown
lsof -i
```

- Conexiones de red activas:
```markdown
ss -tuln
```

- Conexiones de red establecidas
```markdown
netstat -anp
```

- Escaneo rápido de puertos:
```markdown
nmap -sS localhost
```

- Puertos detallado de puertos:
```markdown
nmap -A localhost
```

- Archivos de Log en tiempo real:
```markdown
tail -f /var/log/auth.log
```

- Volcado de discos/particiones:
```markdown
sudo dd if=/dev/sda of=/home/usuario/disco.img bs=4M
```

---

<!---------------------------------- USO DE HASHES ----------------------------------------->

## HASHES:

- Verificar la integridad del volcado:
```markdown
sha256sum /home/usuario/disco.img
```

---

<!------------------------------------ FTK IMAGER ------------------------------------------->

## FTK IMAGER:

> FTK Imager es una herramienta gratuita de AccessData que permite:
> - Capturar imágenes forenses de discos duros y memoria RAM.
> - Permite vericar la integridad de las imágenes mediante hashes.
> - No realiza análisis forense avanzado; solo crea y examina las imágenes.

- Capturar memoria RAM:
```markdown
1. Abrir FTK Imager como administrador.
2. Seleccionar "Capture Memory".
3. Guardar el archivo de volcado de memoria RAM.
```

---

<!---------------------------------------- LiME --------------------------------------------->

## LiME:

> LiME es una herramienta gratuita que permite:
> - Capturar la memoria RAM en vivo.
> - El uso de varios formatos de volcado como **raw** o **lime**.
> - No realiza análisis forense avanzado; solo crea y examina las imágenes.

- Capturar memoria RAM:
```markdown
sudo insmod lime.ko "path=/home/usuario/LiME/memoria.lime format=lime"
```

---

<!------------------------------------ VOLATILITY -------------------------------------------->

## VOLATILITY:

> Volatility es una herramienta de análisis forense de memoria que permite examinar
volcados de RAM.

- Identificación del Sistema Operativo:
```markdown
python3 vol.py -f memdump.mem imageinfo
```

- Lista de procesos:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion pslist
```

- Lista procesos ocultos:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion psscan
```

- Lista conexiones de red activas:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion netscan
```

- Búsqueda archivos DLL:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion dlllist -p <pid>
```

- Comandos ejecutados via terminal:
```markdown
sudo pip2 install distorm3
python3 vol.py -f memdump.mem --profile=SOversion cmdscan
```

- Buscar inyecciones de malware:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion malfind
```

- Buscar y extraer archivos abiertos o en uso del volcado de memoria:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion filescan
```

- Extraer archivos específicos del volcado de memoria:
```markdown
python3 vol.py -f memdump.mem --profile=SOversion procdump -p <pid> --dumpdir /home/super/extraccion
```

---

<!------------------------------------- STANDALONE ------------------------------------------->

## STANDALONE:

- Identificación del Sistema Operativo:
```markdown
volatility -f memdump.mem imageinfo
```

- Lista de procesos:
```markdown
volatility -f memdump.mem --profile=SOversion pslist
```

- Comandos ejecutados via terminal:
```markdown
volatility -f memdump.mem --profile=SOversion cmdscan
```

- Lista conexiones de red activas:
```markdown
volatility -f memdump.mem --profile=SOversion netscan
```

---

<!--------------------------------------- AUTOPSY -------------------------------------------->

## AUTOPSY:

---

<!--------------------------------------- DESCARGAS ------------------------------------------>

## DESCARGAS:

- ### FTK Imager:

| [Web Oficial - FTK Imager]([https://www.youtube.com/watch?v=HKRZohqJEMM&t=160s](https://www.exterro.com/digital-forensics-software/ftk-imager)) |
|-----------|

- ### LiME:

1. sudo apt-get install build-essential linux-headers-$(uname -r) git
2. git clone https://github.com/504ensicsLabs/LiME.git
3. cd LiME/src
4. make

- ### Volatility:

| [Tutorial - Volatility v3](https://www.youtube.com/watch?v=HKRZohqJEMM&t=160s) |
|-----------|

1. wget ...
2. sudo apt install python3
3. sudo apt install python3-pip python-setuptools build-essential
4. sudo python3 setup.py install
5. python3 vol.py

- ### Volatility Standalone:

| [Zip Standalone v2.6](http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_lin64_standalone.zip) |
|-----------|

- ### Autopsy:

| [Tutorial - Autopsy v4.21](https://www.youtube.com/watch?v=DYMG7U7FOPU) |
|-----------|

1. wget https://raw.githubusercontent.com/sleuthkit/autopsy/develop/linux_macos_install_scripts/install_prereqs_ubuntu.sh
2. chmod +x install_prereqs_ubuntu.sh
3. ./install_prereqs_ubuntu.sh
4. sudo apt update
5. sudo apt install ./sleuthkit-java_4.12.1-1_amd64.deb
6. wget https://raw.githubusercontent.com/sleuthkit/autopsy/develop/linux_macos_install_scripts/install_application.sh
7. chmod +x install_application.sh
8. ./install_application.sh -z autopsy-4.21.0.zip -i ~/autopsy -j /usr/lib/jvm/java-1.17.0-openjdk-amd64
9. ./bin/autopsy --nosplash

---

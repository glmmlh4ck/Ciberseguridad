# MEMORIA RAM

En esta guía encontraremos todos las herramientas para analizar la memoria RAM.

---

## ÍNDICE:
> | WINDOWS |
> |-----------|
1. [FTK Imager](#ftk-imager)
> | LINUX |
> |-----------|
2. [LiME](#lime)
3. [Volatility](#volatility)
4. [Volatility Standalone](#standalone)
> | DESCARGAS |
> |-----------|
5. [Instalación de los programas](#descargas)

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
sudo insmod lime.ko "path=<ruta_guardar.lime> format=lime"
```

---

<!------------------------------------ VOLATILITY -------------------------------------------->

## VOLATILITY:

> Volatility es una herramienta de análisis forense de memoria que permite examinar
volcados de RAM.

- Identificación del Sistema Operativo:
```markdown
python3 vol.py -f <img_ram> imageinfo
```

- Lista de procesos:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> pslist
```

- Lista procesos ocultos:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> psscan
```

- Lista conexiones de red activas:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> netscan
```

- Búsqueda archivos DLL:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> dlllist -p <pid>
```

- Comandos ejecutados via terminal:
```markdown
sudo pip2 install distorm3
python3 vol.py -f <img_ram> --profile=<img_profile> cmdscan
```

- Buscar inyecciones de malware:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> malfind
```

- Buscar y extraer archivos abiertos o en uso del volcado de memoria:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> filescan
```

- Extraer archivos específicos del volcado de memoria:
```markdown
python3 vol.py -f <img_ram> --profile=<img_profile> procdump -p <pid> --dumpdir <ruta_guardar>
```

---

<!------------------------------------- STANDALONE ------------------------------------------->

## STANDALONE:

> Igual que Volatility sin usar el módulo de python, entre otras cosas.

- Identificación del Sistema Operativo:
```markdown
volatility -f <img_ram> imageinfo
```

- Lista de procesos:
```markdown
volatility -f <img_ram> --profile=<img_profile> pslist
```

- Comandos ejecutados via terminal:
```markdown
volatility -f <img_ram> --profile=<img_profile> cmdscan
```

- Lista conexiones de red activas:
```markdown
volatility -f <img_ram> --profile=<img_profile> netscan
```

---

<!--------------------------------------- DESCARGAS ------------------------------------------>

## DESCARGAS:

- ### FTK Imager:

| [Web Oficial - FTK Imager](https://www.exterro.com/digital-forensics-software/ftk-imager) |
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

---

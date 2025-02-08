# Análisis Forense

En esta guía encontraremos todos los usos sobre herramientas de forense.

---

## Índice
1. [Detección de hashes](#hashes)
2. [Análisis de memoria - Volatility](#volatility)
3. [Análisis de memoria - Volatility Standalone](#standalone)
4. [Análisis de discos - Autopsy](#autopsy)
5. [Enlaces e Imágenes](#enlaces-e-imagenes)
6. [Código](#codigo)
7. [Citas](#citas)
8. [Tablas](#tablas)
9. [Descargas](#descargas)

---

## Hashes

---

## Volatility

---

## Standalone

- Identificación del Sistema Operativo:
```markdown
volatility -f memdump.mem imageinfo
```

- Lista de procesos:
```markdown
volatility -f memdump.mem --profile=SOversion pslist
```

- Comandos usados en CMD:
```markdown
volatility -f memdump.mem --profile=SOversion cmdscan
```

- Identificación de las conexiones:
```markdown
volatility -f memdump.mem --profile=SOversion netscan
```

---

## Autopsy

---

## Descargas

- ### Volatility:
[Tutorial - Volatility v3](https://www.youtube.com/watch?v=HKRZohqJEMM&t=160s)

| [Tutorial - Volatility v3](https://www.youtube.com/watch?v=HKRZohqJEMM&t=160s) | Columna 2 |
|-----------|-----------|
| Dato 1    | Dato 2    |

1. wget ...
2. sudo apt install python3
3. sudo apt install python3-pip python-setuptools build-essential
4. sudo python3 setup.py install
5. python3 vol.py

- ### Volatility Standalone:
[Zip Standalone v2.6](http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_lin64_standalone.zip)

- ### Autopsy:
[Tutorial - Autopsy v4.21](https://www.youtube.com/watch?v=DYMG7U7FOPU)

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

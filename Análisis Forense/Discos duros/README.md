# ANÁLISIS DISCOS DUROS
En esta guía encontraremos todos las herramientas para analizar los discos duros.

---

## ÍNDICE:
> | WINDOWS & LINUX |
> |-----------|
1. [Autopsy](#autopsy)
> | DESCARGAS |
> |-----------|
2. [Instalación de los programas](#descargas)

<!--------------------------------------- AUTOPSY -------------------------------------------->

## AUTOPSY:

---

<!--------------------------------------- DESCARGAS ------------------------------------------>

## DESCARGAS:

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

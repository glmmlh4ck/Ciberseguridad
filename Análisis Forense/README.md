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

> Similar a Volatility sin usar python.

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

### Volatility:
[Tutorial - Volatility v3](https://www.youtube.com/watch?v=HKRZohqJEMM&t=160s)

1. wget ...
2. sudo apt install python3
3. sudo apt install python3-pip python-setuptools build-essential
4. sudo python3 setup.py install
5. python3 vol.py

### Volatility Standalone:
[.zip Standalone v2.6](http://downloads.volatilityfoundation.org/releases/2.6/volatility_2.6_lin64_standalone.zip)

### Autopsy:
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

## Listas----------------------------------------------------------------------------

### Listas no ordenadas
Usa `-`, `+` o `*`.
```markdown
- Elemento 1
- Elemento 2
```
### Resultado:
- Elemento 1
- Elemento 2

### Listas ordenadas
Usa números seguidos de un punto (`1.`).
```markdown
1. Elemento 1
2. Elemento 2
```
### Resultado:
1. Elemento 1
2. Elemento 2

---

## Enlaces e Imágenes------------------------------------------------------------------

### Enlaces
Crea enlaces con `[Texto](URL)`.
```markdown
[Google](https://www.google.com)
```
### Resultado:
[Google](https://www.google.com)

### Imágenes
Crea imágenes con `![Texto alternativo](URL)`.
```markdown
![Logo de Markdown](https://markdown-here.com/img/icon256.png)
```
### Resultado:
![Logo de Markdown](https://markdown-here.com/img/icon256.png)

---

## Código

### Código en línea
Usa `` ` `` para incluir fragmentos de código dentro de un texto.
```markdown
Esto es un ejemplo de `código en línea`.
```
### Resultado:
Esto es un ejemplo de `código en línea`.

### Bloques de código
Usa tres tildes invertidas `` ``` `` para crear bloques.
```markdown
```python
# Este es un bloque de código en Python
print("Hola, Markdown!")
```
```
### Resultado:
```python
# Este es un bloque de código en Python
print("Hola, Markdown!")
```

---

## Citas
Usa `>` para crear citas o bloques destacados.
```markdown
> Esto es una cita destacada.
```
### Resultado:
> Esto es una cita destacada.

---

## Tablas
Crea tablas usando `|` y `-`.
```markdown
| Columna 1 | Columna 2 |
|-----------|-----------|
| Dato 1    | Dato 2    |
```
### Resultado:
| Columna 1 | Columna 2 |
|-----------|-----------|
| Dato 1    | Dato 2    |

---

## Listas de tareas
Usa `- [ ]` para tareas pendientes y `- [x]` para tareas completadas.
```markdown
- [x] Tarea completada
- [ ] Tarea pendiente
```
### Resultado:
- [x] Tarea completada
- [ ] Tarea pendiente

---

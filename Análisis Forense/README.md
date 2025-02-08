# Análisis Forense

# Guía de Sintaxis Markdown

Esta guía incluye toda la sintaxis de Markdown con descripciones y ejemplos.

---

## Índice
1. [Encabezados](#encabezados)
2. [Texto en negrita y cursiva](#texto-en-negrita-y-cursiva)
3. [Listas](#listas)
4. [Enlaces e Imágenes](#enlaces-e-imagenes)
5. [Código](#codigo)
6. [Citas](#citas)
7. [Tablas](#tablas)
8. [Listas de tareas](#listas-de-tareas)

---

## Encabezados
Se crean utilizando el símbolo `#`. La cantidad de `#` determina el nivel del encabezado.
```markdown
# Encabezado Nivel 1
## Encabezado Nivel 2
### Encabezado Nivel 3
```
### Resultado:
# Encabezado Nivel 1
## Encabezado Nivel 2
### Encabezado Nivel 3

---

## Texto en negrita y cursiva
- **Negrita**: Usa `**` o `__`.
- *Cursiva*: Usa `*` o `_`.
- **_Combinado_**: Usa `**_` o `__*`.

```markdown
**Este texto es en negrita**
*Este texto es en cursiva*
**_Este texto es en negrita y cursiva_**
```
### Resultado:
**Este texto es en negrita**
*Este texto es en cursiva*
**_Este texto es en negrita y cursiva_**

---

## Listas

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

## Enlaces e Imágenes

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

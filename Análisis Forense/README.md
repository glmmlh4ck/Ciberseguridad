# ANÁLISIS FORENSE

> En este repositorio encontraremos todos las herramientas que se usan para el análisis forense en sus carpetas correspondientes; así como su análisis previo. 

---

## ÍNDICE:
1. [Análisis previo](#análisis-previo)
2. [Detección de hashes](#hashes)

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
sudo dd if=/dev/sda of=<ruta_guardar.img> bs=4M
```

---

<!---------------------------------- USO DE HASHES ----------------------------------------->

## HASHES:

- Verificar la integridad del volcado:
```markdown
sha256sum <ruta_img>
```

---

---

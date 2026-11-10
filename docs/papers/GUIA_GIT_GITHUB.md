# Guía rápida: Git y GitHub

Repositorio: https://github.com/mjwidow/tarea_ml_10_11
Carpeta local: `C:\proyectos_ia\tarea_ml_10_11`

Ejecuta los comandos en **CMD** o PowerShell, dentro de la carpeta del repositorio.

---

## 1. Verificar que Git funciona

```
git --version
```

Si dice que no reconoce `git`, cierra la terminal y abre una nueva.

---

## 2. Ir a la carpeta del repositorio

```
cd C:\proyectos_ia\tarea_ml_10_11
```

---

## 3. Ver el estado

```
git status
```

Muestra qué archivos cambiaron, cuáles están listos para subir y cuáles no están rastreados.

---

## 4. Descargar cambios de GitHub (pull)

```
git pull
```

Trae a tu equipo los cambios que otra persona subió al repositorio. Hazlo **antes** de empezar a trabajar.

---

## 5. Preparar archivos (add)

Agregar todos los cambios:
```
git add -A
```

Agregar solo un archivo:
```
git add ruta\del\archivo.py
```

---

## 6. Guardar cambios localmente (commit)

```
git commit -m "Descripción corta de lo que cambiaste"
```

Ejemplos de mensajes: `"Agrega análisis de biomarcadores"`, `"Corrige función de limpieza de datos"`.

---

## 7. Subir cambios a GitHub (push)

```
git push
```

La primera vez, para la rama `main`, usa:
```
git push -u origin main
```

---

## 8. Flujo completo típico

```
cd C:\proyectos_ia\tarea_ml_10_11
git pull
git add -A
git commit -m "Mi cambio"
git push
```

---

## 9. Ver el historial

```
git log --oneline
```

---

## 10. Deshacer cosas (con cuidado)

- Quitar un archivo del siguiente commit, sin borrarlo:
  ```
  git restore --staged archivo.txt
  ```
- Descartar cambios no guardados de un archivo (**borra los cambios de forma permanente**):
  ```
  git restore archivo.txt
  ```

---

## Problemas comunes

| Mensaje | Solución |
|---|---|
| `git no se reconoce como un comando` | Abre una terminal nueva o reinicia el equipo. |
| `fatal: not a git repository` | Estás en una carpeta que no es el repositorio. Haz `cd C:\proyectos_ia\tarea_ml_10_11`. |
| `Updates were rejected because the remote contains work...` | Alguien subió cambios antes. Ejecuta `git pull` y luego `git push`. |
| `Permission denied` o pide contraseña | GitHub no acepta contraseñas; usa un **token personal** como contraseña. |
| `nothing to commit` | No hay cambios nuevos que guardar. |

---

## Buenas prácticas

- Haz `git pull` antes de empezar a trabajar.
- Haz commits pequeños con mensajes claros.
- No subas contraseñas, tokens ni archivos `.env` al repositorio.

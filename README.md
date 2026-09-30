# Gestión de Llaves · Grupos de Promociones

App web estática para hoteles que reciben grupos de promociones (estudiantes, etc.).  
Permite dar de alta grupos, asignar habitaciones y personas, y registrar **quién entrega / recibe la llave** con hora automática.

## Características

- **Grupos** con fechas y notas
- **Habitaciones** con lista de personas
- **Entrega / recepción de llaves** con timestamp
- **Búsqueda global** (Ctrl+K) por habitación, persona o grupo
- **Filtro “solo llaves fuera”**
- **Resumen de pendientes** (todas las llaves que no están en recepción)
- **Borrar / editar grupos y habitaciones**
- **Tema claro / oscuro**
- **Exportar / importar JSON** (backup)
- **Modo offline** (Service Worker + localStorage)
- Interfaz **keyboard-first**

### Atajos de teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl + K` | Buscar |
| `T` | Cambiar tema |
| `P` | Ver pendientes |
| `E` | Entregar llave (persona enfocada) |
| `R` | Recibir llave (persona enfocada) |
| `Enter` | Alternar entregar/recibir |
| `↑` `↓` | Navegar personas / resultados |
| `Esc` | Cerrar modal o volver |

## Publicar en GitHub Pages

1. Crea un repositorio (ej. `hotel-llaves`).
2. Sube estos archivos a la **raíz**:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `README.md` (opcional)
3. Ve a **Settings → Pages**.
4. Source: **Deploy from a branch** → `main` → `/ (root)`.
5. En 1–2 minutos estará en:  
   `https://TU-USUARIO.github.io/hotel-llaves/`

## Uso local

Abre `index.html` en el navegador, o sirve la carpeta:

```bash
npx serve .
# o
python3 -m http.server 8080
```

> El Service Worker funciona mejor con un servidor HTTP (no con `file://`).

## Datos

Todo se guarda en **localStorage** del navegador.  
Usa **Exportar** para hacer copias de seguridad en JSON e **Importar** para restaurarlas en otro dispositivo.

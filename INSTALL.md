# 🚀 Guía Rápida de Instalación

## Para GitHub Pages (Solo Lectura)

1. **Crea un repositorio en GitHub:**
   - Nombre: `guardias-2026` (o el que prefieras)
   - Público o privado

2. **Sube estos archivos:**
   ```
   index.html
   guardias.json
   vacaciones.json
   festivos.json
   README.md
   ```

3. **Activa GitHub Pages:**
   - Repositorio → Settings → Pages
   - Source: Deploy from a branch
   - Branch: main → / (root)
   - Save

4. **Espera 1-2 minutos** y accede a:
   ```
   https://TU-USUARIO.github.io/guardias-2026/
   ```

## Para Uso Local (Con Edición)

### Método 1: Sin servidor (Recomendado)
1. Descarga `index_standalone.html`
2. Haz doble click
3. ¡Listo! Ya puedes intercambiar guardias

### Método 2: Con servidor
```bash
python -m http.server 8000
```
Abre: http://localhost:8000

## ¿Qué funciona dónde?

| Funcionalidad | GitHub Pages | Local |
|---------------|--------------|-------|
| Ver guardias | ✅ | ✅ |
| Exportar .ics | ✅ | ✅ |
| Intercambiar guardias | ❌ | ✅ |
| Resetear cambios | ❌ | ✅ |

## Preguntas Frecuentes

**¿Cómo modifico las guardias permanentemente?**
- Edita `guardias.json` y súbelo a GitHub

**¿Los intercambios se pierden al cerrar el navegador?**
- No, se guardan en localStorage (local)
- Pero solo en TU navegador

**¿Puedo tener ambos?**
- Sí, usa GitHub Pages para consultar
- Y abre el archivo local para editar

**¿Cómo actualizo GitHub Pages con mis cambios?**
- Edita los JSON
- Súbelos al repositorio
- Los cambios aparecerán automáticamente

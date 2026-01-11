# Sistema de Gestión de Guardias 2025-2026

## 📋 Descripción
Aplicación web para visualizar guardias, festivos y vacaciones del personal.

## 📦 Archivos incluidos
- `index.html` - Aplicación principal
- `guardias.json` - Datos de guardias
- `vacaciones.json` - Períodos vacacionales
- `festivos.json` - Festivos oficiales

## 🚀 Instrucciones de uso

### Opción 1: Servidor web local (RECOMENDADO)
Debido a restricciones CORS, necesitas usar un servidor web local:

**Con Python 3:**
```bash
python -m http.server 8000
```

**Con Python 2:**
```bash
python -m SimpleHTTPServer 8000
```

**Con Node.js (npx):**
```bash
npx http-server -p 8000
```

**Con PHP:**
```bash
php -S localhost:8000
```

Luego abre tu navegador en: `http://localhost:8000`

### Opción 2: Extensión de navegador
Instala una extensión como "Live Server" para Visual Studio Code

### Opción 3: Modificar el código (NO RECOMENDADO)
Si necesitas abrirlo directamente como archivo, tendrías que integrar los JSON directamente en el HTML.

## 📱 Funcionalidades

### Secciones disponibles:
- **📊 Resumen**: Estadísticas generales y vista rápida
- **👥 Personas**: Listado de personas con sus guardias
- **📅 Calendario**: Vista mensual con todas las guardias
- **🎯 Hoy**: Quién tiene guardia actualmente
- **🎊 Festivos**: Festivos que coinciden con guardias
- **🏖️ Vacaciones**: Períodos vacacionales de cada persona

### Características:
- ✅ Navegación por meses
- ✅ Visualización de guardias por persona
- ✅ Marcado de festivos
- ✅ Indicador de día actual
- ✅ Responsive (adaptado a móviles)
- ✅ Diseño moderno con gradientes

## 🎨 Personalización

### Modificar colores
Edita las variables CSS en el `<style>` del HTML:
```css
:root {
    --primary-color: #4CAF50;
    --secondary-color: #2196F3;
    --danger-color: #e74c3c;
    /* ... */
}
```

### Añadir personas
Edita `guardias.json` y añade nuevas entradas:
```json
{
  "NOMBRE": [
    ["2026-01-15", "2026-01-21"]
  ]
}
```

### Añadir festivos
Edita `festivos.json`:
```json
{
  "2026-12-31": "Nombre del festivo"
}
```

## 🔧 Solución de problemas

### No se cargan los datos
- Verifica que los archivos JSON estén en la misma carpeta que index.html
- Asegúrate de usar un servidor web local (no abras el archivo directamente)
- Abre la consola del navegador (F12) para ver errores

### El calendario no muestra información
- Verifica que las fechas en los JSON tengan formato correcto: "YYYY-MM-DD"
- Comprueba que los JSON sean válidos (usa un validador JSON online)

## 📄 Formato de datos

### guardias.json
```json
{
  "PERSONA": [
    ["fecha_inicio", "fecha_fin"],
    ["2026-01-15", "2026-01-21"]
  ]
}
```

### vacaciones.json
```json
{
  "PERSONA": [
    ["fecha_inicio", "fecha_fin", "descripción"],
    ["2026-07-01", "2026-07-15", "Vacaciones verano"]
  ]
}
```

### festivos.json
```json
{
  "2026-01-01": "Año Nuevo",
  "2026-12-25": "Navidad"
}
```

## 💡 Consejos
- Mantén copias de seguridad de los archivos JSON
- Las fechas deben seguir el formato ISO: YYYY-MM-DD
- Los períodos de guardias pueden solaparse
- El sistema detecta automáticamente qué persona tiene guardia cada día

## 🐛 Reportar problemas
Si encuentras algún error, revisa:
1. Formato de los JSON (fechas correctas)
2. Que estés usando un servidor web local
3. Consola del navegador (F12) para ver errores

---
**Versión:** 1.0.0  
**Fecha:** Enero 2026  
**Compatibilidad:** Todos los navegadores modernos

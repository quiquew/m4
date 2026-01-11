# 📅 Sistema de Gestión de Guardias 2026

Sistema web para visualizar y gestionar guardias, festivos y vacaciones de técnicos.

## 🌐 Demo en Vivo

Visita: `https://tu-usuario.github.io/guardias-2026/`

## ✨ Características

### Modo GitHub Pages (Solo Lectura)
- ✅ Visualización de guardias en calendario
- ✅ Vista por personas con todas sus guardias
- ✅ Exportar guardias a calendario (formato .ics)
- ✅ Exportar vacaciones a calendario
- ✅ Ver quién tiene guardia hoy
- ✅ Festivos durante guardias
- ✅ Estadísticas dinámicas por año

### Modo Local (Con Edición)
Todas las anteriores MÁS:
- ✅ **Intercambiar guardias entre técnicos**
- ✅ Los cambios se guardan en localStorage
- ✅ Botón para resetear a guardias originales

## 🚀 Instalación en GitHub Pages

1. **Fork o crea un nuevo repositorio** en GitHub

2. **Sube estos archivos:**
   ```
   index_standalone.html    (renombrar a index.html)
   guardias.json
   vacaciones.json
   festivos.json
   README.md
   ```

3. **Activa GitHub Pages:**
   - Ve a Settings → Pages
   - Source: Deploy from a branch
   - Branch: main (o master) → carpeta / (root)
   - Guarda los cambios

4. **Accede a tu sitio:**
   - URL: `https://tu-usuario.github.io/nombre-repo/`
   - Espera 1-2 minutos para que se despliegue

## 💻 Uso Local con Edición

### Opción 1: Doble Click (Más Fácil)
1. Descarga `index_standalone.html`
2. Haz doble click en el archivo
3. Se abrirá en tu navegador con capacidad de edición

### Opción 2: Servidor Local
```bash
# Con Python 3
python -m http.server 8000

# Con Python 2
python -m SimpleHTTPServer 8000

# Con Node.js
npx http-server -p 8000

# Con PHP
php -S localhost:8000
```

Luego abre: `http://localhost:8000`

## 🔄 Intercambio de Guardias (Solo Modo Local)

1. Ve a la sección **"Personas"**
2. Verás botones **"🔄 Cambiar"** junto a cada guardia
3. Click en el botón de la guardia que quieres cambiar
4. Selecciona el técnico con quien quieres intercambiar
5. Selecciona la guardia específica a intercambiar
6. Click en **"Confirmar Intercambio"**
7. ¡Listo! Los cambios se guardan automáticamente

### Resetear Cambios
Si quieres volver a las guardias originales:
- Click en el botón **"🔄 Resetear Cambios"** (solo visible en modo local)

## 📱 Exportar a Calendario

Cada técnico puede exportar sus guardias y vacaciones:

1. En la sección **"Personas"**
2. Click en **"📅 Exportar Guardias"** o **"🏖️ Exportar Vacaciones"**
3. Se descarga un archivo `.ics`
4. Abre el archivo para importarlo a:
   - Google Calendar
   - Outlook
   - Apple Calendar
   - Cualquier app compatible con iCalendar

## 📊 Formato de Datos

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

## 🎨 Personalización

### Modificar Datos
Edita los archivos JSON y vuelve a subirlos a GitHub. Los cambios se reflejarán automáticamente.

### Cambiar Colores
Edita las variables CSS en `index.html`:
```css
:root {
    --primary-color: #4CAF50;
    --secondary-color: #2196F3;
    --danger-color: #e74c3c;
}
```

## 🔧 Tecnologías

- HTML5
- CSS3 (Grid, Flexbox, Gradients)
- JavaScript Vanilla (ES6+)
- LocalStorage API
- iCalendar (.ics) format

## 📝 Notas Importantes

- **GitHub Pages**: Los intercambios de guardias NO funcionan (es estático)
- **Modo Local**: Los intercambios se guardan en el navegador (localStorage)
- **Navegadores**: Compatible con Chrome, Firefox, Safari, Edge
- **Responsive**: Funciona en móviles y tablets

## 🐛 Solución de Problemas

### No se ven los datos en GitHub Pages
- Verifica que `index.html` esté en la raíz del repositorio
- Revisa que los archivos JSON estén en la misma carpeta
- Espera 1-2 minutos después de activar Pages

### Los cambios no se guardan en GitHub
- Normal, GitHub Pages es de solo lectura
- Usa modo local para editar
- Para cambios permanentes, modifica los JSON y súbelos a GitHub

### No aparecen los botones de intercambio
- Solo funcionan en modo local (file:// o localhost)
- En GitHub Pages no aparecerán (es correcto)

## 📄 Licencia

Libre uso para gestión de guardias de equipos técnicos.

## 👨‍💻 Autor

Sistema desarrollado para gestión de guardias técnicas 2026.

---

**Versión:** 2.0.0  
**Última actualización:** Enero 2026  
**Compatibilidad:** GitHub Pages + Local con edición

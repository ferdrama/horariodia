# Huecos & Tareas - Documentación

**Huecos & Tareas** es una aplicación web de planificación diaria que te permite organizar tu tiempo mediante "huecos" (bloques de tiempo) y asignar tareas a esos bloques.

## 🎯 Características principales

### Gestión de Tareas
- **Crear tareas** con título y duración estimada en minutos
- **Editar y eliminar** tareas existentes
- **Marcar como completadas** mediante checkbox
- **Filtrar tareas** por estado: Pendientes, Hechas o Todas
- **Reordenar tareas** arrastrándolas en la lista
- **Altura proporcional**: Las tarjetas de tareas tienen altura proporcional a su duración

### Gestión de Huecos (Bloques de Tiempo)
- **Crear huecos** con título, hora de inicio y duración
- **Visualización en timeline**: Vista tipo calendario con escala horaria
- **Mover huecos** arrastrándolos verticalmente en el timeline
- **Redimensionar huecos** desde el borde inferior
- **Editar y eliminar** huecos existentes
- **Indicador de hora actual**: Línea roja que muestra la hora actual
- **Rango configurable**: Ajustar las horas de inicio y fin del timeline

### Asignación de Tareas a Huecos
- **Asignar tareas** a huecos de tiempo de dos formas:
  1. Haciendo clic en el hueco y seleccionando la tarea
  2. **Arrastrando la tarea** directamente sobre el hueco
- **Control de capacidad**: Cada hueco muestra minutos asignados vs disponibles
- **Asignaciones parciales**: Una tarea puede dividirse entre varios huecos
- **Indicador visual**: Las tareas completamente asignadas se marcan con ✓

### Persistencia
- **Almacenamiento local**: Todos los datos se guardan en localStorage
- **Persistencia por día**: Los datos se organizan por fecha
- **Sin necesidad de cuenta**: Todo funciona offline

### PWA (Progressive Web App)
- **Instalable**: Se puede instalar como aplicación nativa
- **Funciona offline**: Service Worker para caché de recursos
- **Iconos optimizados**: Iconos de 192px y 512px

## 🖥️ Interfaz

### Layout
- **Diseño responsive**: Una columna en móvil, dos columnas en escritorio
- **Panel izquierdo**: Formularios y lista de tareas
- **Panel derecho**: Timeline visual con huecos de tiempo

### Timeline
- **Escala visual**: 1.5 píxeles por minuto
- **Grid horario**: Líneas cada hora para referencia visual
- **Slots interactivos**: Los huecos muestran título, horario, capacidad y tareas asignadas

## 🛠️ Tecnologías

- **HTML5**: Estructura semántica
- **CSS3**: Variables CSS, Flexbox, Grid
- **JavaScript vanilla**: Sin frameworks ni dependencias
- **LocalStorage API**: Persistencia de datos
- **Service Workers**: Funcionamiento offline
- **Web App Manifest**: Instalación como PWA

## 📁 Estructura de archivos

```
horariodia/
├── index.html          # Aplicación principal (HTML + CSS + JS integrado)
├── manifest.json       # Configuración PWA
├── sw.js              # Service Worker para caché offline
├── icons/
│   ├── icon-192.png   # Icono pequeño
│   ├── icon-512.png   # Icono grande
│   ├── icon-192.svg   # Icono vectorial pequeño
│   └── icon-512.svg   # Icono vectorial grande
└── docs/
    └── README.md      # Esta documentación
```

## 🚀 Uso

1. Abre `index.html` en un navegador moderno
2. Añade tareas con el formulario superior
3. Crea huecos de tiempo indicando título, hora y duración
4. Asigna tareas a los huecos arrastrándolas o haciendo clic
5. Reorganiza tareas y huecos según necesites

## 📱 Instalación como PWA

1. Abre la aplicación en Chrome o Edge
2. Haz clic en el icono de instalación en la barra de direcciones
3. Confirma la instalación
4. ¡Listo! La app aparecerá en tu escritorio/pantalla de inicio

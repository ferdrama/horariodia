# Huecos & Tareas - Documentación

**Huecos & Tareas** es una aplicación web de planificación diaria que te permite organizar tu tiempo mediante "huecos" (bloques de tiempo) y asignar tareas a esos bloques.

## 🎯 Características principales

### Gestión de Tareas
- **Crear tareas** con título y duración estimada en minutos o pomodoros
- **Editar y eliminar** tareas existentes
- **Marcar como completadas** mediante checkbox
- **Filtrar tareas** por estado: Pendientes, Hechas o Todas
- **Reordenar tareas** arrastrándolas en la lista
- **Altura proporcional**: Las tarjetas de tareas tienen altura proporcional a su duración
- **Ver asignaciones**: Cada tarea muestra a qué huecos está asignada con chips interactivos
- **Desasignar desde tarea**: Botón ✕ en cada chip para eliminar la asignación

### Gestión de Huecos (Bloques de Tiempo)
- **Crear huecos** con título, hora de inicio y duración
- **Visualización en timeline**: Vista tipo calendario con escala horaria
- **Mover huecos** arrastrándolos verticalmente en el timeline
- **Redimensionar huecos** desde el borde inferior
- **Editar y eliminar** huecos existentes
- **Indicador de hora actual**: Línea roja que muestra la hora actual
- **Rango configurable**: Ajustar las horas de inicio y fin del timeline
- **Tareas proporcionales**: Las tareas asignadas ocupan espacio visual proporcional a su duración

### Asignación de Tareas a Huecos
- **Asignar tareas** a huecos de tiempo de dos formas:
  1. Haciendo clic en el hueco y seleccionando la tarea
  2. **Arrastrando la tarea** directamente sobre el hueco
- **Asignación completa**: Al arrastrar, se asigna toda la tarea (sin recortar)
- **Control de overbooking**: Si el hueco queda excedido, aparece un modal con opciones:
  - 📐 Ampliar el hueco para que quepa la tarea
  - ✂️ Ajustar la duración de la tarea
  - ⏭️ Dejar así y ajustar después manualmente
- **Asignaciones parciales**: Una tarea puede dividirse entre varios huecos
- **Indicador visual**: Las tareas completamente asignadas se marcan con ✓
- **Ajuste automático**: Al editar la duración de una tarea, las asignaciones se ajustan proporcionalmente

### Sistema de Pomodoros 🍅
- **Duración configurable**: Define cuántos minutos tiene un pomodoro (default: 25 min)
- **Toggle de unidades**: Alterna entre mostrar tiempos en minutos o en pomodoros
- **Conversión automática**: Toda la interfaz se adapta al modo seleccionado
- **Inputs inteligentes**: Los formularios aceptan valores en la unidad actual
- **Persistencia**: La configuración se guarda en localStorage

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
- **Altura proporcional**: Cada tarea asignada ocupa espacio proporcional a sus minutos

### Tarjetas de Tareas
- **Información completa**: Título, duración estimada, tiempo restante
- **Chips de asignaciones**: Muestran a qué huecos está asignada cada tarea
- **Acciones rápidas**: Asignar, editar, eliminar y desasignar

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
6. Si un hueco queda excedido, elige cómo resolverlo en el modal

## 📱 Instalación como PWA

1. Abre la aplicación en Chrome o Edge
2. Haz clic en el icono de instalación en la barra de direcciones
3. Confirma la instalación
4. ¡Listo! La app aparecerá en tu escritorio/pantalla de inicio

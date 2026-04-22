# Changelog

Todos los cambios relevantes del plugin distribuidos a usuarios finales se documentan en este archivo.

El formato sigue [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/) y este proyecto usa [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

El plugin distribuido por este repositorio tiene su propia numeración de versiones, independiente del repositorio de desarrollo.

---

## [V1.0] — 2026-04-22

### Primera versión distribuida al equipo

Esta es la primera release de **A11Y Copilot** disponible para el equipo de diseño. El plugin permite anotar, validar y documentar la accesibilidad de tus pantallas de Figma sin salir del editor, y que el equipo de desarrollo lo vea directamente en Dev Mode.

### Funcionalidades

- **Tagging de roles semánticos** en cualquier frame de Figma (22 roles disponibles: Button, Link, Checkbox, Text field, Image, Heading, Accordion, Tab bar, etc.).
- **Contenedores semánticos** (Wrapper, List, Screen) para agrupar estructura.
- **Orden de lectura y foco** editable por nodo, con validación en tiempo real de duplicados.
- **Labels y textos alternativos** por tipo (`info` para descripción, `func` para funcional).
- **Niveles de encabezado** (h1-h6, p) asignables al rol Heading.
- **Menú de opciones extra (⋯) por tag**: Dev docs (enlace a documentación por rol o container), Notes (notas de producto), Custom attributes (pares clave-valor libres).
- **Auto-relleno de Dev docs** al asignar rol o container con URL por defecto predefinido en el catálogo. Botón Restore para reponer el default si lo habías modificado.
- **Vista de specs** (modo read-only) con resumen estructural del árbol accesible.
- **Blueprint nativo en Dev Mode**: las annotations de Figma se generan desde el plugin y se leen en Dev Mode sin necesidad de abrirlo.
- **Herencia componente → instancia** con override local. Los valores heredados se distinguen visualmente de los authored localmente.
- **Validaciones en tiempo real**: labels faltantes, focus/reading duplicados, textAlt requerido en rol Image, etc.
- **5 idiomas**: inglés, español, catalán, gallego y euskera. Cambio de idioma desde Settings.
- **Apariencia**: modo claro/oscuro/auto y densidad compact/normal configurables.

### Instalación

Descarga el ZIP desde [este enlace](https://github.com/roger6vi/A11Y-Copilot-Plugin/archive/refs/heads/main.zip), descomprime e importa el `manifest.json` desde Figma Desktop (`Plugins → Development → Import plugin from manifest…`).

### Reportar un problema

Los bugs y peticiones van al [repositorio de desarrollo](https://github.com/roger6vi/A11Y-Copilot/issues). Necesitas acceso — si no lo tienes, pídelo al responsable del plugin.

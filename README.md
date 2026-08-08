# 🛡️ Vault Guard - El Escudo Definitivo para tu Bóveda de Obsidian

> **¡Mantén tu conocimiento 100% seguro!** Cero eliminaciones accidentales, cero borrados imprevistos por plugins descontrolados, auditoría de integridad al inicio sin falsos positivos y restauración garantizada desde la papelera o el historial de Git.

---

## 🌟 ¿Por qué necesitas Vault Guard?

En Obsidian, tu bóveda es tu segundo cerebro. Con docenas de plugins activos, atajos de teclado y miles de notas interconectadas, **un solo clic erróneo o un plugin mal configurado puede borrar años de conocimiento**.

**Vault Guard** fue creado como un sistema de defensa integral para tu bóveda. Intercepta, analiza, pregunta y registra cualquier intento de eliminación antes de que ocurra una catástrofe.

---

## 🚀 Virtudes y Características Destacadas

### 🛡️ 1. Modo Total Guard (Protección Inexpugnable)
Bloquea de forma absoluta la eliminación de notas `.md`, carpetas y formatos protegidos en toda tu bóveda. Nada se borra a menos que tú lo autorices explícitamente en una confirmación directa.

### 🧩 2. Interceptador Inteligente de Plugins de Terceros
¿Un plugin de automatización o limpieza intentó borrar tus notas sin avisar? Vault Guard lo intercepta en tiempo real y te notifica especificando:
- **¿Qué plugin?** (Ej. `auto-cleaner`)
- **¿Qué función/proceso?** (Ej. `deleteOldFiles()`)
- **¿En qué ubicación de código?** (Ej. `main.js:142`)
- *"El plugin X intenta borrar la nota Y ¿lo permites?"*

### 🏷️ 3. Distinción Semántica Nativa (Concordancia Exacta)
Vault Guard trata a cada elemento con la terminología y concordancia gramatical precisa en notificaciones nativas de Obsidian, modales y registros de historial:

- 📝 **Notas Markdown**:
  - *"La nota `MiNota.md` fue eliminada"*
  - *"La nota `Ideas.md` fue restaurada exitosamente."*

- 📄 **Archivos Generales** (`.pdf`, `.rar`, `.png`, `.canvas`, etc.):
  - *"El archivo `Documento.pdf` fue eliminado"*
  - *"El archivo `Archivos.rar` fue eliminado"*
  - *"El archivo `Esquema.png` fue restaurado exitosamente."*

- 📁 **Carpetas**:
  - *"La carpeta `Proyectos` fue eliminada"*
  - *"La carpeta `Recursos` fue restaurada exitosamente."*

### ⚠️ 4. Confirmaciones Secuenciales con Botones Visibles
Olvídate de borrar carpetas o múltiples archivos por error:
- **Botones de Alta Visibilidad**: Botones **Sí** (Verde/Rojo) y **No** (Azul) altamente contrastados para evitar clics accidentales.
- **Detalle Explícito**: Muestra el conteo exacto de notas, archivos y subcarpetas afectadas dentro de una carpeta.
- **Cola Secuencial**: Si se intentan eliminar múltiples archivos simultáneamente, Vault Guard te preguntará uno por uno.

### 🔎 5. Auditoría de Integridad al Inicio (Blindaje 0-Falsos Positivos)
Al abrir Obsidian, Vault Guard realiza una auditoría comparando el último registro de bóveda (`snapshot.json`), el Grafo de Enlaces MOC y el estado de Git. 
- **Detector Anti-Falsos Positivos (`fileExistsInVault`)**: Si moviste un archivo a otra carpeta, le cambiaste el nombre o lo renombraste mediante Git (`git status/diff -M`), Vault Guard lo reconoce automáticamente y **evita lanzar falsas alarmas de archivo perdido**.

### 🤖 6. Compatibilidad y Exclusión Automática de Zoottelkeeper
Detecta dinámicamente las configuraciones y etiquetas identificadoras de Zoottelkeeper (ej. `Índice:`, `_Index_of_`, `#MOC`) y **excluye automáticamente sus archivos de índice** de los análisis de pérdidas o bloqueos molestos.

### 📜 7. Búsqueda Histórica en Git (Estilo `r-calendar`)
Consulta y recupera cualquier archivo eliminado en la historia de tu repositorio Git:
- **Navegación por Pestañas**: Cambia fácilmente entre el *Historial Reciente (Local)* y la *Búsqueda Histórica (Git)*.
- **Selector de Fechas con Calendario**: Filtra eliminaciones por rango de fechas mediante un calendario interactivo estilo `r-calendar`.
- **Búsqueda Pickaxe en Diff**: Con la casilla *"Buscar también en el contenido / diff de los commits"*, busca términos directamente en el contenido de los cambios guardados en Git.
- **Barra de Progreso Reactiva**: Una elegante barra de progreso se activa con un degradado de color vibrante al iniciar cada consulta en Git.

### 🔗 8. Red de Enlaces y Restauración en 1-Clic
Al restaurar una nota principal, Vault Guard analiza sus conexiones directas y referencias (`[[WikiLinks]]` y Virtual Linker) ofreciendo recuperar simultáneamente todos sus archivos vinculados desde la papelera `.trash`.

---

## ⚙️ Instalación y Uso

1. Copia la carpeta `vault-guard` dentro de `.obsidian/plugins/`.
2. Activa **Vault Guard** en los *Plugins de la comunidad*.
3. Haz clic en el icono del **escudo** en la barra lateral o ejecuta el comando `Vault Guard: Abrir panel`.

---

## 📄 Licencia

MIT License © 2026 Baalgarthem.

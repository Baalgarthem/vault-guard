# 🛡️ Vault Guard - El Escudo Definitivo para tu Bóveda de Obsidian

> **¡Mantén tu conocimiento 100% seguro!** Cero eliminaciones accidentales, cero borrados imprevistos por plugins descontrolados y restauración garantizada.

---

## 🌟 ¿Por qué necesitas Vault Guard?

En Obsidian, tu bóveda es tu segundo cerebro. Con docenas de plugins activos, atajos de teclado y miles de notas interconectadas, **un solo clic erróneo o un plugin mal configurado puede borrar años de conocimiento**.

**Vault Guard** fue creado como un sistema de defensa integral para tu bóveda. Intercepta, analiza, pregunta y registra cualquier intento de eliminación antes de que ocurra una catástrofe.

---

## 🚀 Virtudes y Características Destacadas

### 🛡️ 1. Modo Total Guard (Protección Inexpugnable)
Bloquea de forma absoluta la eliminación de notas `.md` en toda tu bóveda. Nada se borra a menos que tú lo autorices explícitamente en una confirmación directa.

### 🧩 2. Interceptador Inteligente de Plugins de Terceros
¿Un plugin de automatización o limpieza intentó borrar tus notas sin avisar? Vault Guard lo intercepta en tiempo real y te notifica especificando:
- **¿Qué plugin?** (Ej. `auto-cleaner`)
- **¿Qué función/proceso?** (Ej. `deleteOldFiles()`)
- **¿En qué línea de código?** (Ej. `main.js:142`)
- *"El plugin X intenta borrar la nota Y ¿lo permites?"*

### ⚠️ 3. Confirmaciones Secuenciales con Botones Visibles
Olvídate de borrar carpetas o múltiples archivos por error:
- **Botones de Alta Visibilidad**: Botones **Sí** (Verde/Rojo) y **No** (Azul) altamente contrastados para evitar clics accidentales.
- **Ruta y Nombre Explícito**: Identifica claramente si se trata de una **Nota** (`.md`), un **Archivo** (`.pdf`, `.png`, `.rar`) o una **Carpeta**.
- **Cola Secuencial**: Si se intentan eliminar 10 archivos a la vez, Vault Guard te preguntará uno por uno.

### 🔗 4. Rastreo de Enlaces (`[[WikiLinks]]` y Virtual Linker)
Antes de que un elemento sea eliminado, Vault Guard analiza y registra todos sus enlaces entrantes y salientes para notificarte sobre posibles conexiones o referencias que quedarían rotas.

### 🔄 5. Restauración en 1-Clic desde la Papelera `.trash`
Si una nota es eliminada, puedes recuperarla a su ubicación original directamente desde el panel de Vault Guard con un solo botón.

### 📊 6. Panel Lateral Dedicado (Estilo `r-calendar`)
Accede a un panel visual interactivo desplegable desde la barra lateral con un recuadro desplazable (scroll) para revisar hasta 100 eliminaciones recientes con filtros de búsqueda instantáneos.

### 🏷️ 7. Distinción Semántica Nativa
Vault Guard trata a cada elemento con la terminología precisa en notificaciones nativas:
- *"La nota `MiNota.md` fue eliminada"*
- *"El archivo `Documento.pdf` fue eliminado"*
- *"El archivo `Archivos.rar` fue eliminado"*
- *"La carpeta `Proyectos` fue eliminada"*

---

## ⚙️ Instalación y Uso

1. Copia la carpeta `vault-guard` dentro de `.obsidian/plugins/`.
2. Activa **Vault Guard** en los *Plugins de la comunidad*.
3. Haz clic en el icono del **escudo** en la barra lateral o ejecuta el comando `Vault Guard: Abrir panel`.

---

## 📄 Licencia

MIT License © 2026 Baalgarthem.

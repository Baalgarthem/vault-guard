## 1. Índice de Contenidos

- [2. La Historia Detrás de Vault Guard: El Drama del Conocimiento Perdido](#2-la-historia-detrás-de-vault-guard-el-drama-del-conocimiento-perdido)
- [3. Matriz de Comparación: Tu Bóveda Con y Sin Vault Guard](#3-matriz-de-comparación-tu-bóveda-con-y-sin-vault-guard)
- [4. Las 12 Armas Defensivas de Vault Guard](#4-las-12-armas-defensivas-de-vault-guard)
  - [4.1 Blindaje Total (Total Guard) desde el Segundo Cero](#41-blindaje-total-total-guard-desde-el-segundo-cero)
  - [4.2 Detector Forense Multi-Bandera: ¿Quién intentó eliminar tu nota?](#42-detector-forense-multi-bandera-quién-intentó-eliminar-tu-nota)
  - [4.3 Concordancia Semántica Nativa y Distinción Exacta de Elementos](#43-concordancia-semántica-nativa-y-distinción-exacta-de-elementos)
  - [4.4 Modales de Confirmación Secuencial con Métricas Explícitas](#44-modales-de-confirmación-secuencial-con-métricas-explícitas)
  - [4.5 Auditoría de Integridad al Arrancar (Snapshot Guard & 0-Falsos Positivos)](#45-auditoría-de-integridad-al-arrancar-snapshot-guard--0-falsos-positivos)
  - [4.6 Exclusión Inteligente de MOCs Zoottelkeeper y Papelera (.trash)](#46-exclusión-inteligente-de-mocs-zoottelkeeper-y-papelera-trash)
  - [4.7 Motor Unificado de Búsqueda Histórica en Git hasta el Commit Inicial](#47-motor-unificado-de-búsqueda-histórica-en-git-hasta-el-commit-inicial)
  - [4.8 Filtro de Fechas de 5 Escenarios y Búsqueda en Contenido (Pickaxe Diff)](#48-filtro-de-fechas-de-5-escenarios-y-búsqueda-en-contenido-pickaxe-diff)
  - [4.9 Reconstrucción Inteligente de Redes de Enlaces WikiLinks](#49-reconstrucción-inteligente-de-redes-de-enlaces-wikilinks)
  - [4.10 Selector de Densidad Visual Configurable (4 Escalas de Elementos)](#410-selector-de-densidad-visual-configurable-4-escalas-de-elementos)
  - [4.11 Registro Local con Insignia "Recuperado desde repositorio"](#411-registro-local-con-insignia-recuperado-desde-repositorio)
  - [4.12 Compatibilidad Multiplataforma 100% Nativa (Escritorio y Móvil)](#412-compatibilidad-multiplataforma-100-nativa-escritorio-y-móvil)
- [5. Arquitectura de Rendimiento y Memoria en 3 Bloques](#5-arquitectura-de-rendimiento-y-memoria-en-3-bloques)
  - [5.1 Pipeline de Comprobación en Memoria O(1)](#51-pipeline-de-comprobación-en-memoria-o1)
  - [5.2 Recolección de Basura Asíncrona y Destrucción de Streams](#52-recolección-de-basura-asíncrona-y-destrucción-de-streams)
- [6. Guía de Instalación y Configuración Rápida](#6-guía-de-instalación-y-configuración-rápida)
  - [6.1 Instalación en Obsidian](#61-instalación-en-obsidian)
  - [6.2 Configuración Recomendada](#62-configuración-recomendada)
- [7. Preguntas Frecuentes (FAQ)](#7-preguntas-frecuentes-faq)
- [8. Licencia y Créditos](#8-licencia-y-créditos)

---

## 2. La Historia Detrás de Vault Guard: El Drama del Conocimiento Perdido

Imagina esta escena: Has dedicado meses —quizás años— a construir tu **Segundo Cerebro** en Obsidian. Miles de notas entrelazadas, esquemas conceptuales, diarios de proyecto, reflexiones profundas y redes de conocimiento meticulosamente tejidas mediante enlaces WikiLinks.

De repente, un día abres tu bóveda y notas un vacío helado. Un plugin de limpieza automatizada mal configurado ejecutó un borrado en segundo plano. O tal vez, un deslice con el teclado eliminó una carpeta entera con decenas de notas esenciales. O peor aún: un archivo desapareció silenciosamente hace tres semanas mientras sincronizabas tu bóveda entre dispositivos.

**El pánico es instantáneo.** Intentas buscar en la papelera del sistema, pero fue vaciada. Miras tu historial y descubres enlaces rotos esparcidos por todas partes como cables desenchufados en una central eléctrica.

**Aquí es donde nace Vault Guard.** 

Vault Guard no es un simple plugin de respaldo; es el **Guardián Inexpugnable de tu Conocimiento**. Diseñado con arquitectura defensiva de nivel militar, intercepta cualquier borrado en el instante exacto en que se solicita, investiga quién fue el responsable, detiene la catástrofe y te otorga el control absoluto de tu información.

---

## 3. Matriz de Comparación: Tu Bóveda Con y Sin Vault Guard

| Característica / Escenario | Sin Vault Guard ❌ | Con Vault Guard 🛡️ |
|----------------------------|--------------------|---------------------|
| **Eliminación por Plugins de Terceros** | Un plugin puede borrar carpetas enteras en segundo plano sin avisarte. | Intercepción instantánea en el segundo 0 con el nombre exacto del plugin solicitante. |
| **Borrado Accidental de Carpetas** | Un clic en "Eliminar" borra la carpeta y todo su contenido sin métricas claras. | Modal secuencial que contabiliza notas `.md`, subcarpetas y archivos afectados antes de actuar. |
| **Recuperación de Archivos Antiguos** | Si no está en la papelera local, la nota se pierde para siempre. | Búsqueda histórica profunda en Git hasta el **commit inicial de la bóveda**. |
| **Red de Enlaces Al Restaurar** | Al restaurar una nota, sus archivos vinculados permanecen rotos o perdidos. | Reconstrucción automática de redes `[[WikiLinks]]` y Virtual Linker en 1 clic. |
| **Notificaciones de Inicio** | Sorpresas con notas desaparecidas semanas después sin saber qué ocurrió. | Auditoría de integridad al arrancar con detección de estado Git y 0 falsos positivos. |
| **Compatibilidad Móvil (iOS/Android)** | Errores de script por dependencias rígidas de Node.js en celulares. | 100% compatible en escritorio y dispositivos móviles con interfaz táctil adaptativa. |

---

## 4. Las 12 Armas Defensivas de Vault Guard

#### 4.1 Blindaje Total (Total Guard) desde el Segundo Cero
Desde el milisegundo en que Obsidian inicia, Vault Guard aplica un empaquetado de seguridad (*Monkey Patching*) sobre las funciones nativas `app.vault.delete` y `app.vault.trash`. Ninguna nota `.md`, carpeta o formato protegido puede ser eliminado del disco sin pasar primero por la aduana de Vault Guard.

#### 4.2 Detector Forense Multi-Bandera: ¿Quién intentó eliminar tu nota?
Vault Guard analiza la pila de llamadas de JavaScript (*Stack Trace*) y las firmas de contexto para decirte con precisión quirúrgica quién originó el intento de borrado:
- 👤 **Acciones Manuales del Usuario**: *"Solicitado manualmente por el usuario desde el menú contextual"*.
- 🧩 **Plugins de Terceros**: *"Solicitado por el plugin 'auto-cleaner' (función: deleteOldFiles)"*.
- ⚙️ **Procesos de Inicio / Segundo Plano**: *"Solicitado durante el proceso de arranque de la bóveda"*.

#### 4.3 Concordancia Semántica Nativa y Distinción Exacta de Elementos
Olvídate de notificaciones genéricas. Vault Guard respeta la gramática y concordancia exacta en español según el tipo de elemento:
- 📝 **Notas Markdown**: *"La nota `Proyectos.md` fue protegida"*.
- 📄 **Archivos Generales**: *"El archivo `Esquema.png` fue eliminado"*.
- 📁 **Carpetas**: *"La carpeta `Recursos` y sus 15 notas fueron conservadas"*.

#### 4.4 Modales de Confirmación Secuencial con Métricas Explícitas
Si un proceso intenta eliminar una carpeta o múltiples archivos simultáneamente, Vault Guard no se atruena. Muestra un cuadro modal informativo con botones vibrantes de alta visibilidad (Sí / No) indicando el desglose exacto de contenido: notas `.md`, archivos adjuntos y subcarpetas. Si son varios elementos, te preguntará uno a uno de forma organizada.

#### 4.5 Auditoría de Integridad al Arrancar (Snapshot Guard & 0-Falsos Positivos)
¿Cerraste Obsidian y modificaste archivos desde fuera? Al iniciar, Vault Guard compara el estado actual de la bóveda contra un snapshot ligero (`snapshot.json`) y el diferencial de Git. Gracias al algoritmo **`fileExistsInVault`**, si simplemente moviste una nota de carpeta o le cambiaste el nombre, Vault Guard lo reconoce y **elimina los molestos falsos positivos**.

#### 4.6 Exclusión Inteligente de MOCs Zoottelkeeper y Papelera (.trash)
Vault Guard detecta automáticamente las estructuras de índice del plugin Zoottelkeeper (archivos con prefijos como `_index_of_`, `índice:` o etiquetas `#MOC`) y los elementos presentes en la carpeta `.trash`, excluyéndolos de falsas alarmas de pérdida para mantener tu registro limpio.

#### 4.7 Motor Unificado de Búsqueda Histórica en Git hasta el Commit Inicial
La pestaña de *Búsqueda Histórica (Git)* no se limita al estado reciente. Con los parámetros `--all --reflog --full-history`, explora **cada commit existente en la historia de tu repositorio**, descendiendo hasta el mismísimo commit raíz con el que fundaste tu bóveda. Encuentra notas eliminadas hace meses o años en cuestión de instantes.

#### 4.8 Filtro de Fechas de 5 Escenarios y Búsqueda en Contenido (Pickaxe Diff)
Inspirado en la interfaz de calendarios de alta precisión, Vault Guard te permite filtrar búsquedas mediante 5 escenarios estrictos:
1. **Sin Fechas**: Explora la historia completa desde `HEAD` hasta el origen.
2. **Solo Fecha de Inicio**: Busca desde esa fecha hacia atrás hasta el origen.
3. **Solo Fecha de Fin**: Busca desde `HEAD` hacia atrás hasta la fecha de fin.
4. **Rango Estricto**: Filtra únicamente commits entre la fecha de inicio y de fin.
5. **Validación Lógica**: Detecta si la fecha de inicio es posterior a la de fin y te alerta inmediatamente.
*¡Además, con la casilla "Buscar en el contenido / diff", puedes localizar notas buscando palabras clave que estaban escritas dentro de su texto!*

#### 4.9 Reconstrucción Inteligente de Redes de Enlaces WikiLinks
Al restaurar una nota principal, Vault Guard escanea su mapa de conexiones (`[[WikiLinks]]` y referencias de Virtual Linker). Si descubre que los archivos vinculados a esa nota también están en la papelera, te ofrece un botón para **reconstruir la red completa en 1 solo clic**, devolviendo la vida a tu grafo de conocimiento.

#### 4.10 Selector de Densidad Visual Configurable (4 Escalas de Elementos)
Adapta la apariencia del panel lateral a tu flujo de trabajo desde los Ajustes del Plugin:
- 🔵 **Grande (Original)**: Legibilidad amplia y espaciosa.
- 🟢 **Mediano (Recomendado)**: Escala equilibrada (~15% más compacto).
- 🟡 **Pequeño (Compacto)**: Ideal para paneles laterales estrechos.
- 🔴 **Súper Pequeño (Ultra Compacto)**: Máxima densidad de información por pantalla.

#### 4.11 Registro Local con Insignia "Recuperado desde repositorio"
Cada vez que rescatas un archivo desde la pestaña de Git, Vault Guard registra automáticamente el evento en el *Historial Reciente (Local)* estampando una elegante insignia azul: **`Recuperado desde repositorio`**, garantizando trazabilidad total de lo que has restaurado.

#### 4.12 Compatibilidad Multiplataforma 100% Nativa (Escritorio y Móvil)
Diseñado para funcionar sin interrupciones tanto en **Obsidian Desktop** (Windows, macOS, Linux) como en **Obsidian Mobile** (Android e iOS). En móviles, las dependencias de Node.js se aíslan de forma segura y la interfaz ajusta automáticamente sus áreas de toque (*Touch Targets*) para una navegación cómoda en pantallas táctiles.

---

## 5. Arquitectura de Rendimiento y Memoria en 3 Bloques

Para garantizar que Vault Guard no ralentice el arranque de Obsidian ni consuma memoria innecesaria, se diseñó una arquitectura de optimización dividida en tres pilares:

```mermaid
graph LR
    A["Bloque 1: Cachés LRU y TTL"] --> B["Bloque 2: DOM Teardown"]
    B --> C["Bloque 3: Destrucción de Streams StdIO"]
```

#### 5.1 Pipeline de Comprobación en Memoria O(1)
Antes de iterar miles de registros de Git, Vault Guard construye una tabla Hash en memoria (`Set`) con los archivos activos de la bóveda. Las comprobaciones de existencia se realizan a velocidad luz ($O(1)$) en microsegundos, evitando miles de lecturas lentas a disco.

#### 5.2 Recolección de Basura Asíncrona y Destrucción de Streams
- **Cachés Efímeras**: Las reglas de `.gitignore` y metadatos de Zoottelkeeper se purgan automáticamente tras 60 segundos de inactividad.
- **Destrucción de Streams**: Al ejecutar comandos de Git, los flujos `stdout` y `stderr` se destruyen inmediatamente al concluir la consulta (`childProc.stdout.destroy()`), liberando la memoria heap de V8.
- **Limpieza de Nodos DOM**: Al cerrar la vista lateral o un modal, todas las referencias a elementos HTML se anulan para permitir una recolección de basura inmediata.

---

## 6. Guía de Instalación y Configuración Rápida

#### 6.1 Instalación en Obsidian
1. Descarga los archivos `main.js`, `manifest.json` y `styles.css`.
2. Crea una carpeta llamada `vault-guard` dentro de `.obsidian/plugins/` en tu bóveda.
3. Copia los tres archivos dentro de dicha carpeta.
4. Abre Obsidian, ve a **Ajustes → Plugins de la comunidad** y activa **Vault Guard**.

#### 6.2 Configuración Recomendada
- **Total Guard**: Activado (recomendado para máxima protección).
- **Densidad de Interfaz**: Mediano (para una visualización óptima en el panel lateral derecho).
- **Notificaciones de Eliminación**: Activado.
- **Reconstruir Red de Enlaces**: Activado.

---

## 7. Preguntas Frecuentes (FAQ)

- **¿Vault Guard modifica mi repositorio de Git al hacer una búsqueda?**  
  *No. Todas las operaciones de búsqueda y lectura en Git son 100% de solo lectura y no alteran tu árbol de trabajo ni tus commits.*

- **¿Qué ocurre si un plugin intenta borrar una carpeta completa?**  
  *Vault Guard intercepta la solicitud, detiene la ejecución y te muestra un modal indicando el nombre del plugin y el conteo de archivos dentro de la carpeta para que decidas si autorizas o bloqueas la acción.*

- **¿Puedo reabrir una incidencia o sugerir una mejora?**  
  *¡Por supuesto! Conforme a las reglas de desarrollo del proyecto, cualquier tarea o incidencia puede ser reabierta en cualquier momento para seguir perfeccionando el plugin.*

---

## 8. Licencia y Créditos

Desarrollado con ❤️ por **Baalgarthem** (2026).  
Licencia **MIT**. Libre para uso, modificación y distribución.

---
**Versión actual del plugin**: 1.0.0

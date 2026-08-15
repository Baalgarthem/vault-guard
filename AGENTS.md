# Reglas generales para Vault Guard

Estas reglas se aplican a todo el repositorio `vault-guard` y deben respetarse en cada tarea, cambio, revisión y ejecución.

## Prioridad de estas reglas

- Leer y respetar este archivo antes de analizar, programar, probar o modificar el plugin.
- Mantener estas reglas vigentes durante toda la tarea.
- Si una solicitud entra en conflicto con estas reglas, detenerse, explicar el conflicto y pedir instrucciones antes de actuar.

## Límite estricto: carpeta de Obsidian

- `D:\PKM\.obsidian` es exclusivamente una fuente de consulta y análisis de solo lectura.
- Nunca crear, editar, renombrar, mover, copiar dentro de, reemplazar ni eliminar archivos o carpetas en `D:\PKM\.obsidian`.
- Nunca ejecutar comandos, scripts, pruebas, instaladores, formateadores o procesos que puedan escribir directa o indirectamente en `D:\PKM\.obsidian`.
- No instalar ni desplegar el plugin en esa carpeta.
- Antes de ejecutar una herramienta que reciba rutas de entrada y salida, comprobar que ninguna salida apunte a `D:\PKM\.obsidian`.
- Si una validación requiere modificar una bóveda, usar fixtures o una bóveda temporal fuera de `D:\PKM\.obsidian`.

## Alcance de escritura

- Todos los cambios del plugin deben realizarse únicamente dentro de `D:\Scripts\obsidian-plugins\vault-guard`.
- Evitar cambios fuera del alcance solicitado y conservar intactas las modificaciones existentes del usuario.
- No eliminar archivos ni realizar operaciones destructivas salvo que el usuario lo solicite explícitamente y se haya verificado el destino exacto.

## Desarrollo del plugin

- Seguir las APIs y convenciones oficiales de Obsidian y TypeScript usadas por el proyecto.
- Mantener el código claro, modular, tipado y fácil de mantener.
- Validar entradas y manejar errores sin provocar pérdida o corrupción de datos de la bóveda.
- Aplicar el principio de mínimo privilegio: acceder solo a los archivos y capacidades indispensables.
- Evitar dependencias nuevas cuando la plataforma o el proyecto ya proporcionen una solución adecuada.
- No registrar ni exponer contenido privado de la bóveda, secretos, tokens o datos personales.
- Los cambios que puedan afectar archivos de una bóveda deben incluir salvaguardas, rutas normalizadas y comprobaciones explícitas de alcance.

## Verificación

- Ejecutar las comprobaciones disponibles y proporcionales al cambio, como compilación, lint, typecheck y pruebas.
- Las pruebas deben usar datos simulados, fixtures o directorios temporales; nunca `D:\PKM\.obsidian` como destino de escritura.
- Informar con claridad qué se modificó, qué se verificó y cualquier limitación pendiente.

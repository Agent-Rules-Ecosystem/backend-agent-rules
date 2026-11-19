---
name: backend-agent-rules
description: Bootstrap and governance for AI agents in Backend projects (Node.js, Python, APIs REST/GraphQL, microservices, databases).
---

# Backend Agent Rules

## Bootstrap obligatorio

Antes de responder o editar, leer y cumplir:

1. `.agents/core/communication.md` ← **primero siempre; rige todo lo que sigue**
2. `.agents/core/path_map.md`
3. `.agents/core/brain.md`
4. `.agents/core/commands.md`

**Triggers de arranque** — las siguientes frases o condiciones disparan el protocolo completo:

- **"ejecuta .agents"** (o "corre .agents", "bootstrap .agents") → dispara además el Protocolo de Auditoría de Learning definido en `brain.md`.
- "nuevo proyecto" / "inicializar" / "bootstrap" / "empieza" en el primer mensaje.
- Ausencia de `overview/session.md` al comenzar cualquier tarea de código.
- Primer mensaje de conversación cuando el proyecto tiene `.agents/` pero no `overview/`.
- Cualquier mensaje que comience con `$` → reconocer como $-comando según `core/commands.md` y ejecutar el protocolo correspondiente.

Para cualquier tarea que inspeccione o cambie código del proyecto, cargar el estado siguiendo el **Protocolo de Carga de Contexto en 3 Capas** (`core/brain.md`): iniciar con **Capa 1** (`overview/session.md` y `overview/work.md`) y cargar **Capa 2/3** (`overview/work/tasks.md`, `overview/work/deuda_tecnica.md`, `overview/work/pendientes.md`, `overview/trackers/progress.md`, `overview/architecture/` o `overview/work/skill/`) solo según lo exija la tarea o `work_review.md`. Sincronización automática de todos los archivos de control afectados en `overview/` durante `$work` y `$close` es obligatoria. Al finalizar o resolver una tarea proveniente de `pendientes.md` o `deuda_tecnica.md`, mover físicamente la fila correspondiente a `## ✅ Completados (Historial)` y actualizar `work.md`. Si falta `overview/`, crearlo desde `.agents/templates/`. Al finalizar `$boot`, ejecutar el protocolo de `.agents/templates/work_review.md` y registrar el reporte en `overview/work_review.md`.

Las reglas globales viven solo en `.agents/`. **Inviolabilidad estricta de `.agents/`**: Nunca modificar directamente archivos de gobernanza desde un proyecto local.

## Estado local versionado

Crear `overview/` desde `.agents/templates/` al iniciar proyecto:

- `overview/session.md`
- `overview/work.md` (índice maestro)
- `overview/work/tasks.md` (tarea activa: tipo, solución/rutas)
- `overview/work/pendientes.md` (seguimiento al cerrar)
- `overview/work/deuda_tecnica.md` (deuda ordenada por prioridad Alta, Media y Baja)
- `overview/work_review.md` (reporte mutable del `$boot`; el protocolo vive en `.agents/templates/work_review.md`)
- `overview/workflows/` (guías por flujo con terminología 100% agnóstica)
- `overview/trackers/progress.md`
- `overview/architecture.md` (y su estructura Hub & Spoke en `overview/architecture/`)
- `overview/context/` para archivos de contexto general no mapeables
- `overview/learning.md` cuando surja mejora candidata

`overview/history/` conserva sesiones antiguas. Cambios a reglas globales solo ocurren en repositorio oficial.

# 🖥️ Backend Agent Rules

**Cerebro operativo centralizado para agentes de IA en proyectos Backend**. Cubre desarrollo de APIs REST/GraphQL, microservicios, Node.js, Python (FastAPI/Django), bases de datos SQL/NoSQL, autenticación y despliegue en servidores.

Se instala como submódulo de Git en `.agents/`.

---

## 📌 Pilares de Gobernanza

1. **⚡ Modo Lacónico & Token Saver**: Respuestas ultra-concisas y referencias de líneas.
2. **🔄 Sincronización Automática de Rastreadores**: Actualización de archivos `overview/` en `$work` y `$close`.
3. **🗺️ Arquitectura Viva (`$archi`)**: Mapa de servicios, rutas, modelos y dependencias en diagramas Mermaid.
4. **👥 Handoff y Memoria Versionada por Agente**: Firma canónica por proveedor/modelo.
5. **🛡️ Escudo Anti-parches (Filtro Agnóstico)**: Solo procesos de diagnóstico y gobernanza agnósticos en el core.
6. **🔒 Inviolabilidad de `.agents/`**: Los archivos de gobernanza nunca se modifican desde el proyecto local.

---

## ⚡ $-Comandos

| Comando | Descripción |
|---|---|
| `$boot` | Bootstrap completo: reglas, `overview/`, handoff de agente. |
| `$status` | Estado activo en 5 líneas. |
| `$work [descripción]` | Registra tarea/bug y sincroniza rastreadores. |
| `$archi` | Actualiza diagramas Mermaid de servicios y rutas en `overview/architecture.md` (Hub) y `overview/architecture/` (Spoke). |
| `$learn [texto]` | Registra propuesta candidata con Filtro Agnóstico. |
| `$close` | Cierre de sesión y sincronización final. |

---

## ⚡ Quick Start

**1. Instala la gobernanza en tu proyecto**
```bash
git submodule add git@github.com:Agent-Rules-Ecosystem/backend-agent-rules.git .agents
```

**2. Inicia el agente**
```text
$boot
```

**3. Registra tu primera tarea**
```text
$work agregar endpoint REST para gestión de usuarios
```

---


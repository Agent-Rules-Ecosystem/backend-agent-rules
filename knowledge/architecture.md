# Arquitectura de Proyectos Backend

## Capas de Arquitectura

| Capa | Responsabilidad | Ejemplos |
|---|---|---|
| **Transporte** | Manejo de HTTP, WebSockets, RPC | Controllers, Routes, Resolvers (GraphQL) |
| **Aplicación** | Casos de uso y orquestación | Services, Use Cases, Command Handlers |
| **Dominio** | Lógica de negocio pura | Entities, Value Objects, Domain Events |
| **Infraestructura** | Persistencia, APIs externas, mensajería | Repositories, ORM Models, HTTP Clients |

## Patrones Recomendados

- **Repository Pattern**: Abstracción de la persistencia para desacoplar el dominio de la base de datos.
- **Dependency Injection**: Inyectar dependencias para facilitar testing y desacoplamiento.
- **DTO Pattern**: Separar la representación externa (API) de los modelos internos de dominio.
- **Middleware Chain**: Para logging, auth, validación y manejo de errores de forma transversal.

## Reglas de Arquitectura

- Las rutas no contienen lógica de negocio — solo delegación a servicios.
- Los modelos de base de datos no se exponen directamente en la API — usar DTOs.
- Nunca importar infraestructura directamente desde el dominio.

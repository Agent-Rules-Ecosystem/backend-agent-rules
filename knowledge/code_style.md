# Estilo y Convenciones de Código Backend

## Nomenclatura

| Elemento | Convención | Ejemplo |
|---|---|---|
| Clases / Servicios | `PascalCase` | `AuthService`, `UserRepository` |
| Archivos | `kebab-case` (JS/TS) / `snake_case` (Python/Go/Rust) | `auth-service.ts`, `user_model.py`, `auth_handler.go` |
| Variables / funciones | `camelCase` (JS/TS) / `snake_case` (Python) | `getUserById()` / `get_user_by_id()` |
| Constantes | `UPPER_SNAKE_CASE` | `MAX_RETRIES`, `JWT_SECRET` |
| Endpoints REST | `kebab-case` en minúsculas | `/api/user-profiles` |
| Variables de entorno | `UPPER_SNAKE_CASE` | `DATABASE_URL` |

## Manejo de Errores

- Nunca silenciar errores con `catch(e) {}` vacío.
- Usar códigos HTTP semánticamente correctos (200, 201, 400, 401, 403, 404, 422, 500).
- Separar errores de validación, negocio y sistema en capas distintas.
- Siempre loguear errores con contexto suficiente para debugging.

## Async / Concurrencia

- Preferir `async/await` sobre callbacks o `.then()` encadenado.
- Manejar siempre el caso de error en operaciones asíncronas.
- No bloquear el event loop con operaciones síncronas pesadas.

## Seguridad

- Nunca hardcodear secretos, tokens ni contraseñas en el código.
- Validar y sanitizar toda entrada del usuario antes de procesarla.
- Usar variables de entorno para configuración sensible.
- Aplicar principio de mínimo privilegio en permisos de base de datos.

## Organización

- Archivos idealmente < 250 líneas; máximo 300.
- Separar responsabilidades: rutas → controladores → servicios → repositorios.
- No mezclar lógica de negocio en middlewares o manejadores de rutas.

# Estructura Estándar de Proyecto Backend

Especifica las carpetas y archivos nativos estándar reconocidos en proyectos Backend (Node.js/Express, Python/FastAPI, NestJS, etc.). Durante el protocolo de discovery, cualquier carpeta raíz fuera de esta lista es **no-estándar** y debe procesarse mediante inspección semántica.

## Directorios Estándar por Framework

| Directorio | Propósito | Frameworks |
|---|---|---|
| `src/` | Código fuente principal | Node.js, NestJS, FastAPI |
| `app/` | Módulos y lógica principal | Express, Django, FastAPI |
| `routes/` o `controllers/` | Definición de endpoints | Express, Flask |
| `services/` | Lógica de negocio desacoplada de HTTP | Todos |
| `models/` o `entities/` | Modelos de datos / ORM | Todos |
| `middleware/` | Middlewares de autenticación, logging, etc. | Todos |
| `config/` | Configuración de entorno y dependencias | Todos |
| `migrations/` | Migraciones de base de datos | Prisma, TypeORM, Alembic |
| `tests/` o `__tests__/` | Suite de pruebas | Todos |
| `scripts/` | Scripts de utilidad y automatización | Todos |
| `dist/` o `build/` o `__pycache__/` | Salida compilada (ignorar en discovery) | Todos |
| `node_modules/` o `.venv/` | Dependencias (ignorar en discovery) | Todos |
| `.agents/` | Submódulo oficial de reglas compartidas | Conservar en root |
| `overview/` | Estado local versionado del proyecto | Conservar en root |

## Archivos Estándar en Root

- `package.json` / `pyproject.toml` / `requirements.txt`
- `tsconfig.json` / `jest.config.*` / `pytest.ini`
- `.env`, `.env.example`
- `Dockerfile`, `docker-compose.yml`
- `README.md`, `LICENSE`, `.gitignore`

## Regla de Inspección

Cualquier otro directorio en root debe inspeccionarse recursivamente y clasificarse según `core/brain.md`.

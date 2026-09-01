# Checklist pre-release Backend

Cuando el usuario pida desplegar, construir contenedor Docker o preparar release del servicio Backend: ejecutar checklist, mostrar comandos; no desplegar sin solicitud explícita.

- [ ] Linter y verificación de tipos (ej. `npm run lint`, `flake8`, `golangci-lint`, `cargo check`) sin errores nuevos.
- [ ] Suite de pruebas verde (ej. `npm test`, `pytest`, `go test ./...`, `cargo test`), si hay tests.
- [ ] Sin `console.log()` / `print()` de debug olvidados en código de producción.
- [ ] Variables de entorno requeridas documentadas en `.env.example` y configuradas en el servidor/CI.
- [ ] Credenciales y secretos (claves de API, tokens JWT, claves DB) no hardcodeados en repositorio.
- [ ] Migraciones de Base de Datos probadas y listas para ejecución.
- [ ] `overview/trackers/progress.md` y trackers correspondientes actualizados.

## Construcción de Contenedores / Artefactos

```bash
# Ejemplo Docker Build
docker build -t backend-service:latest .

# Ejemplo Test Suite Execution
npm test
```

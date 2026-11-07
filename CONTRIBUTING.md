# Contribución

## Ramas

Parte siempre de `master` actualizado. Usa un nombre corto y descriptivo:

- `feature/<área>-<responsable>` para una historia de usuario.
- `fix/<tema>` para una corrección.
- `docs/<tema>` para documentación.

## Commits

Usa Conventional Commits en español, en imperativo y con alcance:

```text
feat(core): añadir salud y registro de actores
fix(runtime): corregir el empuje entre cascos
test(unity): cubrir la pausa y el reintento
docs: actualizar la guía de pruebas
```

Separa el trabajo en commits pequeños y coherentes. No mezcles cambios de áreas distintas en un mismo commit.

## Pull requests

- Cada PR implementa una historia y referencia su issue con `Closes #<número>`.
- El PR debe describir el cambio, los criterios comprobados y la evidencia.
- Se requiere **Core checks**, **Repository checks** y la aprobación de otra persona.
- Se integra con **merge commit** para conservar la serie de commits.
- No se aceptan builds, cachés, credenciales ni archivos locales.

## Pruebas

Antes de abrir el PR:

```bash
dotnet run --configuration Release --project Tests/CoreChecks/CoreChecks.csproj
```

En Unity, ejecuta las suites **EditMode** y **PlayMode** que correspondan. Si una prueba no se pudo ejecutar, indícalo en el PR; no la declares aprobada.

## Archivos de Unity

Incluye los archivos `.meta` de los recursos que añadas o muevas. Mantén las rutas de `Resources`, escenas y configuración estables para no romper referencias.

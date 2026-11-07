# La Resurrección del Huáscar

Campaña naval 2D en Unity 6000.6.8f1. El jugador comanda el monitor Huáscar en tres misiones ficticias posteriores a la Guerra del Pacífico: interceptar una patrullera, escoltar un convoy y neutralizar baterías costeras.

## Características

- Navegación, apuntado y disparo con `W/A/S/D` y ratón.
- Tres misiones con objetivos, victoria, derrota y reintento.
- Progreso de campaña persistente y desbloqueo secuencial.
- Mapa costero por celdas con colisiones, minimapa y cámara que sigue al Huáscar.
- HUD con salud, objetivos, enemigos, volumen y ayuda al convoy.
- Arte 2D ilustrado, efectos de sonido y música a 1920×1080.

## Equipo

| Responsable | Área |
|---|---|
| Albert Riveros | Base del proyecto, CI y documentación |
| Mauro Sullca | Núcleo de simulación, misiones y progreso |
| Sergio Estrada | Runtime, mapa, escena y pruebas de juego |
| Christian Yana | Arte, interfaz y audio |

## Estructura

```text
Assets/_LRH/
  Scripts/Core/       Reglas de salud, combate, misiones y progreso
  Scripts/Runtime/    Barcos, mapa, cámara, HUD y flujo de campaña
  Editor/             Editor de terreno
  Resources/          Mapas, configuración, arte y audio
  Scenes/Main.unity   Escena principal
  Tests/              Pruebas EditMode y PlayMode
Tests/CoreChecks/     Comprobaciones .NET del núcleo
Tools/                Validación del repositorio y generadores de recursos
docs/                 Requisitos, arquitectura, pruebas y documentación técnica
```

## Abrir el proyecto

1. Instala Unity **6000.6.8f1**.
2. Abre la raíz del repositorio desde Unity Hub.
3. Entra a `Assets/_LRH/Scenes/Main.unity` y pulsa **Play**.

Controles: `W/S` avanzan y retroceden, `A/D` giran, el ratón apunta y el clic dispara. `Esc` pausa.

## Pruebas

Comprobaciones del núcleo:

```bash
dotnet run --configuration Release --project Tests/CoreChecks/CoreChecks.csproj
```

En Unity, abre **Window → General → Test Runner** y ejecuta las suites **EditMode** y **PlayMode**.

## Estado

Proyecto en desarrollo. Las historias de usuario, su prioridad y su avance están en **Issues** y en el tablero del proyecto.

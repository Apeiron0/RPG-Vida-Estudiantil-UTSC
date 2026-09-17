# UTSC-RPG

RPG/simulation 2D top-down sobre la vida universitaria en UTSC.

## Objetivo del proyecto

El jugador controla a un estudiante cuyo objetivo es **aprobar el cuatrimestre y avanzar hacia la graduación**, mientras administra tiempo, energía, estrés, dinero y desempeño académico.

El juego representa problemas cotidianos de una carrera universitaria: tareas, exámenes, transporte, horarios, salones, convivencia y trámites administrativos.

## Alcance

Este proyecto se desarrolla como un **MVP con una ventana total de 3 meses**. La prioridad es tener un juego completo y jugable antes de agregar contenido secundario.

### MVP

- 1 estudiante jugable
- 1 campus pequeño
- 3 materias
- 1 cuatrimestre
- 6–9 tareas
- 3 exámenes
- Sistema de tiempo por bloques
- Energía, estrés, dinero y conocimiento
- Calificaciones y promedio
- Transporte sencillo
- ~5 NPCs
- Diálogos y decisiones simples
- 1 proceso administrativo
- Eventos con consecuencias
- 3–5 finales
- Guardado/carga básico

### Fuera del MVP

- Combate
- Mundo abierto grande
- Multiplayer
- IA avanzada
- Economía compleja
- Inventario avanzado
- Generación procedural
- Varias carreras completamente distintas
- Varios cuatrimestres jugables
- Personalización avanzada
- Grandes cantidades de contenido narrativo

## Stack técnico

- **Engine:** Godot 4.x
- **Lenguaje:** GDScript
- **Género:** RPG / simulación
- **Vista:** 2D Top-Down
- **Datos estáticos:** Godot Resources
- **Guardado:** JSON en `user://savegame.json`
- **Control de versiones:** Git + GitHub + Git LFS
- **Arte:** Aseprite/Krita
- **Audio:** Audacity

## Arquitectura inicial

La arquitectura busca ser simple y mantenible:

- Scenes + Nodes + Scripts
- Signals para comunicación desacoplada
- Autoloads únicamente para sistemas globales
- Resources para datos de materias, tareas, quests y eventos
- Evitar abstracciones innecesarias

Autoloads previstos:

- `GameManager`
- `TimeManager`
- `SaveManager`
- `AcademicManager`

## Estructura

```text
UTSC-RPG/
├── assets/
│   ├── art/
│   ├── audio/
│   ├── fonts/
│   └── ui/
├── data/
│   ├── subjects/
│   ├── quests/
│   ├── dialogue/
│   └── events/
├── docs/
│   ├── GDD.md
│   ├── MVP.md
│   ├── ROADMAP.md
│   └── ARCHITECTURE.md
├── scenes/
│   ├── player/
│   ├── world/
│   ├── npcs/
│   ├── ui/
│   └── systems/
├── scripts/
│   ├── core/
│   ├── player/
│   ├── academic/
│   ├── time/
│   ├── dialogue/
│   ├── quests/
│   ├── npcs/
│   └── ui/
├── saves/
└── project.godot
```

## Flujo de trabajo

```text
feature/* → develop → main
```

- `main`: versión estable/demo.
- `develop`: integración del trabajo del equipo.
- `feature/*`: trabajo individual por funcionalidad.

No se usará GitFlow completo: el proyecto es pequeño y tiene una ventana de 3 meses.

## Regla de alcance

> Si una funcionalidad no mejora directamente el loop del MVP o amenaza el calendario de 3 meses, se pospone.

Consultar `docs/MVP.md` antes de agregar features.

## Estado

**Fase:** planificación + setup técnico  
**Prioridad:** construir primero un vertical slice jugable.

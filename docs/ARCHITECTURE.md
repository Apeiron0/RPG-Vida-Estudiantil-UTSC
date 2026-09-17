# Arquitectura técnica

## 1. Principio

La arquitectura debe ser suficientemente modular para trabajar en equipo, pero no tan abstracta que consuma el calendario del MVP.

## 2. Estructura Godot

```text
scenes/
  player/
  world/
  npcs/
  ui/
  systems/

scripts/
  core/
  player/
  academic/
  time/
  dialogue/
  quests/
  npcs/
  ui/

data/
  subjects/
  quests/
  dialogue/
  events/
```

## 3. Escenas

### Player

```text
Player (CharacterBody2D)
├── CollisionShape2D
├── Sprite2D
├── AnimationPlayer
└── InteractionArea
```

### NPC

```text
NPC (CharacterBody2D)
├── CollisionShape2D
├── Sprite2D
├── InteractionArea
└── DialogueTrigger
```

## 4. Autoloads

Usar pocos globales:

### GameManager
Estado general de partida y coordinación.

### TimeManager
Día, bloque horario y señales:

- `day_changed`
- `time_block_changed`
- `week_changed`

### SaveManager
Serialización/deserialización del estado.

### AcademicManager
Materias, tareas, exámenes y resultados.

## 5. Resources

Usar Godot Resources para datos relativamente estáticos:

- `SubjectData`
- `AssignmentData`
- `QuestData`
- `DialogueData`
- `EventData`

Esto evita hardcodear contenido dentro de los scripts.

## 6. Signals

Preferir signals para eventos del sistema:

```text
TimeManager
   ├── day_changed
   ├── time_block_changed
   └── week_changed
```

Los sistemas interesados se conectan sin acoplar directamente todos los managers.

## 7. Diálogo

Modelo simple:

```text
DialogueResource
      ↓
DialogueManager
      ↓
DialogueUI
```

Las decisiones pueden ejecutar consecuencias:

- modificar dinero
- modificar estrés
- modificar relaciones
- avanzar tiempo
- activar quest

## 8. Guardado

Ruta:

```text
user://savegame.json
```

El save debe contener solamente estado dinámico.

No guardar datos estáticos de materias o diálogos que ya existen en Resources.

## 9. Regla contra overengineering

No introducir:

- arquitectura ECS
- dependency injection framework
- event bus genérico si Signals cubren el caso
- sistema de plugins propio
- backend
- base de datos
- sistemas genéricos sin un caso concreto

La prioridad es entregar el juego.

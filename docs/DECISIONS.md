# Architectural / Project Decisions

## ADR-001 — Godot

**Decisión:** usar Godot 4.x.

**Razón:** permite desarrollar el juego 2D con rapidez, mantener una arquitectura sencilla y trabajar principalmente con GDScript.

## ADR-002 — GDScript

**Decisión:** GDScript como lenguaje principal.

**Razón:** reduce complejidad de integración y es suficiente para el alcance del MVP.

## ADR-003 — 2D Top-Down

**Decisión:** vista 2D top-down.

**Razón:** permite representar campus, NPCs y desplazamiento sin el costo de producción de un entorno 3D.

## ADR-004 — Tiempo por bloques

**Decisión:** 4 bloques diarios.

**Razón:** el objetivo es modelar decisiones de gestión, no simular cada minuto.

## ADR-005 — Un solo cuatrimestre en MVP

**Decisión:** solo un cuatrimestre jugable.

**Razón:** el proyecto tiene una ventana total de 3 meses. Más periodos aumentarían contenido y balance sin ser necesarios para demostrar el concepto.

## ADR-006 — Sin combate

**Decisión:** no implementar combate.

**Razón:** no pertenece al núcleo de la fantasía universitaria y consumiría tiempo de desarrollo.

## ADR-007 — JSON para saves

**Decisión:** guardar estado dinámico en JSON.

**Razón:** simple, legible y suficiente para el tamaño del estado del juego.

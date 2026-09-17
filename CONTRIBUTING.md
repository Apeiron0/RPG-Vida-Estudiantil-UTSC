# Contributing

## Branches

```text
main
└── develop
    ├── feature/player
    ├── feature/time-system
    ├── feature/academic
    ├── feature/dialogue
    └── feature/ui
```

## Reglas

1. No trabajar directamente sobre `main`.
2. Crear una branch `feature/*` por funcionalidad.
3. Mantener commits pequeños y descriptivos.
4. Hacer pull/rebase desde `develop` antes de abrir PR cuando sea necesario.
5. Toda feature nueva debe indicar si pertenece al MVP.
6. No introducir dependencias externas sin discutirlo primero.
7. No modificar escenas grandes sin avisar al equipo.

## Commits

Formato recomendado:

```text
feat: add time block system
fix: prevent duplicate assignment completion
docs: update MVP scope
art: add campus sprites
```

## Pull Requests

Un PR debe incluir:

- qué cambia
- por qué cambia
- cómo probarlo
- si afecta al MVP
- screenshots/video cuando sea relevante

## Conflictos de escenas

Evitar que dos personas editen simultáneamente la misma escena compleja.

Preferir:

- escenas pequeñas
- Resources para datos
- componentes reutilizables
- scripts separados
- señales

# GitHub Setup

## 1. Crear repositorio

Nombre sugerido:

`UTSC-RPG`

Configuración:

- Private, salvo que el curso requiera público.
- README: ya incluido en este repositorio.
- `.gitignore`: ya incluido y orientado a Godot.
- License: decidir según requisitos del curso.

## 2. Inicializar localmente

```bash
git init
git branch -M main
git add .
git commit -m "chore: initialize UTSC-RPG MVP"
git remote add origin <URL_DEL_REPO>
git push -u origin main
```

## 3. Crear develop

```bash
git checkout -b develop
git push -u origin develop
```

## 4. Activar Git LFS

```bash
git lfs install
git lfs track "*.png"
git lfs track "*.aseprite"
git lfs track "*.psd"
git lfs track "*.wav"
git lfs track "*.ogg"
git lfs track "*.fbx"
git add .gitattributes
git commit -m "chore: configure git lfs"
git push
```

`.gitattributes` ya contiene reglas iniciales.

## 5. Protección recomendada

En GitHub:

- proteger `main`
- requerir Pull Request
- evitar push directo a `main`
- opcionalmente requerir aprobación antes de merge

Para un equipo pequeño, no es necesario complicar las reglas.

## 6. GitHub Projects

Crear un Project tipo Board:

```text
BACKLOG → TODO → IN PROGRESS → REVIEW → DONE
```

Campos recomendados:

- Status
- Priority
- Area
- MVP
- Milestone
- Assignee

## 7. Labels

Crear:

- `feature`
- `bug`
- `gameplay`
- `technical`
- `art`
- `audio`
- `UI`
- `documentation`
- `MVP`
- `priority-high`
- `priority-medium`
- `priority-low`

## 8. Milestones

Crear:

- `M1 - Foundations`
- `M2 - Core Gameplay`
- `M3 - Final MVP`

## 9. Regla de proyecto

El Project Board no debe convertirse en una lista infinita de ideas.

Todo issue debe pertenecer a:

- MVP actual, o
- backlog claramente marcado como Post-MVP.

# Game Design Document — UTSC-RPG

## 1. Visión

UTSC-RPG es un RPG/simulador 2D top-down sobre la vida universitaria.

El jugador no lucha contra un villano tradicional. El principal desafío es administrar la acumulación de responsabilidades, restricciones y decisiones de una carrera universitaria.

## 2. Fantasía del jugador

> “Tengo que sacar adelante el cuatrimestre, pero cada decisión que tomo afecta mi tiempo, energía, dinero, estrés y desempeño.”

## 3. Objetivo

El objetivo inmediato es **aprobar el cuatrimestre**. El objetivo de largo plazo representado por el juego es **terminar la carrera**.

Para el MVP solo se juega un cuatrimestre; la progresión hacia la graduación funciona como marco narrativo.

## 4. Pilares de diseño

### Gestión
El jugador administra recursos limitados.

### Decisiones
Las actividades compiten por el mismo recurso crítico: tiempo.

### Consecuencias
Las decisiones deben producir efectos observables.

### Identidad universitaria
El campus, las materias, profesores, transporte y trámites deben hacer que el problema se sienta universitario.

### Alcance controlado
El juego debe ser pequeño pero completo.

## 5. Gameplay

### Acciones principales

- estudiar
- asistir a clase
- dormir
- trabajar
- socializar
- hacer tareas
- presentar exámenes
- realizar trámites
- desplazarse

### Recursos

| Recurso | Función |
|---|---|
| Energía | Limita actividades y recuperación |
| Estrés | Aumenta por presión y malas decisiones |
| Dinero | Permite cubrir necesidades/transporte |
| Conocimiento | Influye en rendimiento académico |
| Tiempo | Recurso central |
| Promedio | Resultado académico |

## 6. Sistema de tiempo

Un día se divide en 4 bloques:

```text
MAÑANA → MEDIODÍA → TARDE → NOCHE
```

Cada actividad consume uno o más bloques.

Al finalizar el bloque correspondiente, se procesan:

- cambios de energía
- estrés
- eventos
- deadlines
- asistencia
- cambios de día/semana

## 7. Sistema académico

MVP:

- 3 materias
- 2–3 actividades evaluables por materia
- 1 examen principal por materia
- calificación final por materia

La fórmula exacta de calificación se considera una variable de balance.

## 8. Transporte

El transporte es un sistema de apoyo, no el foco principal.

Opciones simplificadas:

- caminar
- transporte público
- automóvil

Eventos posibles:

- retraso
- llegada a tiempo
- costo
- pérdida de un bloque

No se construirá una simulación realista de rutas.

## 9. NPCs

Conjunto inicial aproximado:

1. Profesor/a
2. Compañero/a organizado/a
3. Compañero/a de equipo
4. Amigo/a
5. Personal administrativo

Cada NPC debe tener una función jugable o narrativa clara.

## 10. Trámites

El MVP incluye 1 proceso administrativo de varios pasos.

Ejemplo abstracto:

```text
Hablar con administración
      ↓
Conseguir documento
      ↓
Entregar documento
      ↓
Esperar / volver
      ↓
Resolver trámite
```

El trámite debe representar burocracia mediante decisiones y tiempo, no mediante texto excesivo.

## 11. Eventos

Los eventos introducen variación y presión:

- profesor cambia una fecha
- transporte retrasado
- tarea inesperada
- oportunidad de trabajo
- invitación social
- problema administrativo

Cada evento debe tener una consecuencia o elección.

## 12. Finales

Se pueden utilizar 3–5 estados finales basados en desempeño y decisiones.

Ejemplos conceptuales:

- aprobar el cuatrimestre
- repetir por desempeño académico
- aprobar con alto costo personal
- resultado equilibrado

Los finales deben reutilizar sistemas existentes, no requerir sistemas nuevos.

## 13. Dirección artística

- 2D top-down
- estilo sencillo y consistente
- campus pequeño
- sprites reutilizables
- UI legible
- prioridad a claridad sobre detalle

## 14. UX

La UI debe mostrar siempre, como mínimo:

- día/periodo
- bloque horario
- energía
- estrés
- dinero
- conocimiento
- tareas próximas
- promedio cuando corresponda

## 15. Guardado

Estado mínimo:

```json
{
  "day": 1,
  "time_block": 0,
  "money": 100,
  "energy": 100,
  "stress": 0,
  "knowledge": 0,
  "grades": {}
}
```

El formato es orientativo; la implementación final puede cambiar.

## 16. Criterio de diseño

Si una mecánica agrega complejidad pero no produce una decisión interesante, debe cuestionarse antes de entrar al MVP.

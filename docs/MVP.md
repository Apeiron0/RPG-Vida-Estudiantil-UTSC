# MVP — UTSC-RPG

## 1. Propósito

El MVP debe demostrar que el concepto funciona como juego: el jugador puede vivir un cuatrimestre universitario, tomar decisiones con recursos limitados, enfrentar consecuencias académicas y llegar a un resultado final.

El MVP no busca representar toda la universidad. Busca demostrar el **core loop**.

## 2. Core loop

```text
PLANEAR
   ↓
ELEGIR ACTIVIDAD
   ↓
CONSUMIR TIEMPO / RECURSOS
   ↓
RECIBIR CONSECUENCIA
   ↓
AJUSTAR PLAN
   ↓
AVANZAR EL CUATRIMESTRE
```

Ejemplos:

- Estudiar → +conocimiento, -energía, -tiempo.
- Dormir → +energía, -tiempo.
- Trabajar → +dinero, -energía, -tiempo.
- Socializar → mejora relaciones, consume tiempo.
- Ignorar una tarea → riesgo académico y estrés.
- Transporte retrasado → pérdida de tiempo.
- Trámite → cadena corta de pasos con costo de tiempo.

## 3. Contenido mínimo

| Elemento | MVP |
|---|---|
| Jugador | 1 |
| Campus | 1 mapa pequeño |
| Materias | 3 |
| Cuatrimestre | 1 |
| Tareas | 6–9 |
| Exámenes | 3 |
| NPCs | ~5 |
| Trámites | 1 proceso |
| Finales | 3–5 |
| Transporte | Sí, simplificado |
| Guardado | Sí |

## 4. Sistemas obligatorios

### Tiempo
4 bloques por día:

- Mañana
- Mediodía
- Tarde
- Noche

El sistema no simula cada minuto. El objetivo es crear decisiones y presión temporal sin convertir el proyecto en un simulador administrativo.

### Recursos

- Energía
- Estrés
- Dinero
- Conocimiento

La calificación académica es un resultado del desempeño, no un recurso que el jugador gaste directamente.

### Académico

Cada materia tendrá:

- tareas
- evaluación parcial/examen
- evaluación final
- calificación final

Los valores exactos pueden balancearse posteriormente.

### Mundo

El campus debe permitir:

- moverse
- interactuar
- encontrar NPCs
- acceder a aulas/zonas relevantes
- iniciar actividades

## 5. Vertical slice

Antes de construir todo el contenido, debe existir un flujo completo mínimo:

1. Entrar al juego.
2. Controlar al estudiante.
3. Avanzar el tiempo.
4. Elegir estudiar/dormir/socializar.
5. Completar una tarea.
6. Obtener una consecuencia en estadísticas.
7. Presentar un examen.
8. Ver una calificación.
9. Llegar al cierre de un periodo.

Si este flujo funciona, el proyecto tiene una base viable.

## 6. Fuera de alcance

No agregar al MVP:

- combate
- inventario complejo
- árbol de habilidades extenso
- múltiples mapas grandes
- multiplayer
- IA avanzada
- generación procedural
- economía detallada
- múltiples carreras independientes
- múltiples cuatrimestres jugables
- personalización profunda
- cinemáticas complejas

## 7. Regla de cambio de alcance

Toda nueva feature debe responder:

1. ¿Mejora el core loop?
2. ¿Es necesaria para demostrar el concepto?
3. ¿Puede implementarse sin comprometer el calendario?

Si la respuesta no es claramente positiva, va al backlog post-MVP.

## 8. Criterio de terminado del MVP

El MVP está terminado cuando:

- el jugador puede completar el cuatrimestre;
- las decisiones consumen tiempo y modifican recursos;
- tareas y exámenes producen calificaciones;
- existen consecuencias visibles;
- existe al menos un proceso administrativo;
- existe transporte básico;
- existe guardado/carga;
- existen finales;
- el juego puede ejecutarse de principio a fin sin bloqueadores conocidos.

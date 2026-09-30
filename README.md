# Generador de exámenes · Movimiento Ondulatorio

Cuestionario interactivo que genera exámenes aleatorios de Movimiento Ondulatorio con corrección automática.

## Características

- 20 preguntas por examen, repartidas entre 5 secciones del temario.
- Preguntas de opción múltiple y de respuesta numérica.
- Corrección automática con tolerancia para redondeos.
- Explicación del razonamiento en cada pregunta.
- Modo examen y modo práctica (con hoja de fórmulas).
- Puntuación de 1 a 5 y aciertos por sección.
- Lista de temas a repasar según las fallas.
- Modo claro y oscuro.
- Progreso guardado: se puede pausar y continuar.

## Temario

1. Conceptos fundamentales
2. Ondas viajeras y función de onda
3. Velocidad en cuerdas y reflexión/transmisión
4. Superposición, interferencia y energía
5. Ecuación de onda lineal

## Archivos

- `index.html` — estructura de la página
- `estilo.css` — estilos
- `motor.js` — lógica del examen y banco de preguntas

## Uso

Abrir `index.html` en cualquier navegador moderno. No requiere instalación (manteniendo los archivos en la misma carpeta).

También disponible en línea: https://zlaysol.github.io/cuestionario-ondas/

## Añadir preguntas

Las preguntas están en el array `BANK` dentro de `motor.js`. Cada una es un objeto con esta forma:

Opción múltiple:

    { sec: 0, type: "mc", topic: "tema", q: "enunciado",
      opts: ["A", "B", "C", "D"], ans: 0, exp: "explicación" }

Numérica:

    { sec: 0, type: "num", topic: "tema", q: "enunciado",
      fields: [{ label: "v =", unit: "m/s", ans: 4.8, tol: 0.02 }],
      exp: "explicación" }

Para añadir una nueva, copia una existente y modifícala. Añádela al final
del array (no cambies el orden de las anteriores: el progreso guardado
depende de su posición).

## Licencia

Uso libre para fines educativos y académicos.
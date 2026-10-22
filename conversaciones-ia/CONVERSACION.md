# Conversación anterior

## Contexto del proyecto

- Proyecto: `pps1`
- Tema principal: recorrido desde el código fuente hasta la ejecución de un programa.
- Archivo base: [`index.html`](./index.html)
- Idioma de trabajo: español.

## 1. Solicitud inicial: rediseño de la interfaz

Se solicitó rediseñar la interfaz web existente utilizando la skill `fronted-design`.

### Requisitos indicados

- Analizar el framework, componentes, estilos y recursos.
- Identificar los problemas de diseño antes de editar.
- Proponer una dirección visual coherente.
- Mejorar jerarquía visual, tipografía, colores, espacios y adaptación móvil.
- Conservar funcionalidades, rutas, APIs y lógica de negocio.
- Implementar los cambios en los archivos reales.
- Ejecutar las comprobaciones disponibles.
- Presentar primero un plan y esperar aprobación.

### Plan aprobado

Se propuso:

1. Mantener el contenido técnico real.
2. Mejorar la estructura de lectura.
3. Aplicar una estética editorial/técnica.
4. Añadir navegación interna accesible.
5. Mejorar estados `hover` y `focus`.
6. Adaptar el diseño a móvil.
7. Mantener la página autocontenida y sin dependencias externas.

## 2. Rediseño de `index.html`

Después de aprobar el plan, se rediseñó [`index.html`](./index.html).

### Cambios realizados

- Nueva estética oscura con tonos azul petróleo.
- Colores de acento cian y ámbar.
- Tipografía diferenciada para texto y código.
- Nuevo encabezado visual.
- Índice de navegación interna.
- Estructura semántica con `header`, `main`, `article`, `section` y `nav`.
- Enlace para saltar directamente al contenido.
- Bloques de código con mejor legibilidad.
- Tabla adaptable mediante desplazamiento horizontal.
- Diseño responsive para dispositivos móviles.
- Estados de foco visibles para accesibilidad.
- Soporte para `prefers-reduced-motion`.
- Sin dependencias externas ni recursos remotos.

### Validaciones

- Comprobación del diff completada.
- Etiquetas HTML balanceadas.
- Enlaces internos resueltos.
- IDs únicos.
- Sin espacios finales.

## 3. Opciones para crear una skill

Después se solicitó crear una skill relacionada con el contenido de `index.html`.

Se propusieron estas opciones:

1. **Tutor del ciclo de ejecución**
   - Explicaciones adaptadas al nivel del usuario.

2. **Generador de material didáctico**
   - Resúmenes, glosarios, fichas y mapas conceptuales.

3. **Generador de ejercicios y cuestionarios**
   - Preguntas tipo test, verdadero/falso y ejercicios de relación.

4. **Analizador del flujo de compilación**
   - Análisis de código desde el preprocesado hasta la ejecución.

5. **Revisor técnico y pedagógico**
   - Revisión de exactitud, claridad y posibles confusiones.

6. **Skill combinada**
   - Explicación, análisis, material didáctico, ejercicios y revisión técnica.

Se recomendó la opción 6 porque reunía las necesidades principales del proyecto.

## 4. Skill `guia-codigo-a-ejecucion`

Se creó la skill:

[`SKILL.md`](./.github/skills/guia-codigo-a-ejecucion/SKILL.md)

### Configuración

- Nombre: `guia-codigo-a-ejecucion`
- Invocable manualmente con:

  ```text
  /guia-codigo-a-ejecucion
  ```

- También puede cargarse automáticamente para consultas sobre:
  - Compilación.
  - Ensamblado.
  - Enlazado.
  - Memoria de procesos.
  - Stack y heap.
  - Depuración.
  - Descompilación.
  - Análisis forense de memoria.

### Capacidades incluidas

- Explicar conceptos del contenido de `index.html`.
- Analizar fragmentos de código.
- Crear resúmenes y material de estudio.
- Generar ejercicios.
- Revisar la precisión técnica y pedagógica.
- Citar las secciones de la guía utilizadas.
- Distinguir entre contenido original, simplificaciones y ampliaciones.
- Evitar inventar resultados de compilación o disposiciones exactas de memoria.

### Límites definidos

- No modificar archivos sin una petición explícita.
- No inventar contenido ni ejemplos.
- No confundir ensamblador con código máquina.
- No presentar la descompilación como recuperación exacta.
- No tratar el análisis forense de memoria como acceso no autorizado.

## 5. Creación de `ejemplo.html`

Se solicitó crear un ejemplo utilizando la skill `guia-codigo-a-ejecucion`.

Se creó:

[`ejemplo.html`](./ejemplo.html)

### Contenido del ejemplo

La página muestra el recorrido de un pequeño programa que suma dos números:

1. Código fuente.
2. Preprocesado.
3. Compilación y ensamblado.
4. Código objeto y enlazado.
5. Carga, memoria y ejecución.
6. Depuración, descompilación y límites del modelo.

### Características

- Página HTML independiente.
- Diseño visual coherente con `index.html`.
- Ejemplos de código en C.
- Bloques de código con desplazamiento horizontal.
- Explicaciones didácticas.
- Advertencias sobre las diferencias entre compiladores, arquitecturas y entornos.
- Diseño adaptable a móvil.
- Sin dependencias externas.

### Validaciones

- Comprobación del diff completada.
- Verificación de la estructura HTML completada.
- Metadatos esenciales presentes.
- Sin espacios finales detectados.

## Resultado final

Durante la conversación se trabajó sobre estos archivos:

- [`index.html`](./index.html): interfaz principal rediseñada.
- [`ejemplo.html`](./ejemplo.html): ejemplo del flujo de compilación y ejecución.
- [`SKILL.md`](./.github/skills/guia-codigo-a-ejecucion/SKILL.md): skill educativa y técnica.


# Registro del proceso: del código fuente a la ejecución

## Método de documentación

Este registro se ha generado y revisado aplicando la skill
`documentar-proceso-conversaciones`, definida en
`skills/nombre-skill/SKILL.md`. Se han inventariado todos los archivos Markdown
disponibles en `conversaciones-ia/` y se han relacionado con las fases
correspondientes sin copiar las conversaciones completas dentro de este
archivo.

## 1. Alcance y participantes

El objetivo del trabajo es preparar material didáctico sobre el recorrido de un
programa desde el código fuente hasta su ejecución y documentar el uso de IA
con trazabilidad.

**Participación:** Adrian Saibol, con apoyo de GitHub Copilot Chat mediante
Copilot SDK en VS Code. No se atribuyen decisiones a integrantes que no estén
identificados en las conversaciones conservadas.

## 2. Fases registradas

### Fase 1. Recopilación y delimitación del contenido

- **Objetivo:** identificar los conceptos que debía cubrir el material:
  código fuente, preprocesado, compilación, Assembly, ensamblado, código
  objeto, enlazado, carga, ejecución, memoria, depuración y descompilación.
- **Herramienta:** GitHub Copilot Chat en VS Code para organizar los apuntes
  proporcionados; lectura de `contenido/pps1_01 proceso compilación.md`.
- **Prompt:** “Quiero que actúes como un programador web profesional que va
  crear una página web didáctica con ejemplos prácticos sobre el proceso del
  código fuente a la ejecución sobre estos apuntes”.
- **Resultado:** se definió como hilo conductor el recorrido
  código fuente → transformaciones → ejecutable → memoria → CPU, con ejemplos
  en C y Assembly.
- **Decisión:** conservar el alcance técnico de los apuntes y separar el
  recorrido principal de los conceptos de memoria, depurador y descompilador.
- **Justificación:** esta separación evita presentar conceptos de ejecución y
  análisis como si fueran etapas obligatorias del compilado.
- **Verificación:** se contrastó el inventario con el contenido de
  `contenido/pps1_01 proceso compilación.md` y con `evidencias/fuentes.md`.
- **Participación:** Adrian Saibol y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/prompt-completo.md`.

### Fase 2. Diseño de la skill didáctica

- **Objetivo:** crear una skill reutilizable que convierta los apuntes en
  explicaciones y actividades didácticas técnicamente prudentes.
- **Herramienta:** GitHub Copilot Chat mediante Copilot SDK en VS Code,
  aplicando la guía de diseño frontend y la guía de personalización de
  skills.
- **Prompt:** “En base a esto quiero que desarrolles un skill didáctica
  relacionada con el contenido siguiendo los puntos 3.2 y 3.3 sobre el
  registro del proceso y la conservación de conversaciones originales”.
- **Resultado:** se elaboró `skills/nombre-skill/SKILL.md` con frontmatter,
  flujo de trabajo, resultados de aprendizaje, actividades, requisitos de
  accesibilidad, verificación y límites de precisión.
- **Decisión:** mantener la carpeta existente `skills/nombre-skill/` para no
  romper la estructura entregada, pero asignar a la skill el nombre funcional
  `proceso-compilacion-didactica`.
- **Justificación:** así se conserva la ruta esperada por el proyecto y se
  elimina el contenido de plantilla que no aportaba comportamiento didáctico.
- **Verificación:** se revisó que el frontmatter incluya `name` y
  `description`, que la descripción contenga términos de activación y que la
  skill diferencie preprocesador, compilador, ensamblador, enlazador, objeto,
  ejecutable, stack y heap.
- **Participación:** Adrian Saibol y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/skill-didactica.md`.

### Fase 3. Prueba de la skill

- **Objetivo:** comprobar que la skill no se limita a describir conceptos,
  sino que produce una guía aplicable a una experiencia de aprendizaje.
- **Herramienta:** revisión directa del archivo de skill y contraste con los
  apuntes del proyecto.
- **Prompt:** “Desarrolla una skill didáctica relacionada con el contenido y
  documenta el proceso, la conversación de origen y la verificación”.
- **Resultado:** la skill exige una pregunta guía, un ejemplo conductor, dos
  actividades con autocorrección, una navegación accesible para web y una
  comprobación de precisión.
- **Decisión:** aceptar la propuesta y registrar las comprobaciones en
  `evidencias/prueba-skill-propia.md`.
- **Justificación:** las comprobaciones son observables y cubren tanto el
  aprendizaje como la calidad técnica de la salida.
- **Verificación:** se comprobó manualmente el frontmatter, el recorrido de
  etapas, las advertencias sobre modelos simplificados de memoria y la
  distinción entre código objeto y ejecutable.
- **Participación:** Adrian Saibol.
- **Conversación de origen:** `conversaciones-ia/skill-didactica.md`.

### Fase 4. Integración y trazabilidad documental

- **Objetivo:** dejar el proyecto preparado para que otra persona pueda
  contrastar las decisiones con el resultado y las conversaciones.
- **Herramienta:** edición de `README.md`, `PROCESO.md`,
  `evidencias/prueba-skill-propia.md` y
  `conversaciones-ia/skill-didactica.md`.
- **Prompt:** “Conservad todas las conversaciones con IA y relacionad en
  `PROCESO.md` las decisiones y resultados con su archivo de origen”.
- **Resultado:** cada fase incluye los nueve campos solicitados y apunta a una
  conversación concreta.
- **Decisión:** conservar la conversación existente `prompt-completo.md` y
  añadir la conversación específica de la skill en
  `conversaciones-ia/skill-didactica.md`.
- **Justificación:** se evita mezclar el encargo de la página con el diseño y
  prueba de la skill, facilitando la auditoría del proceso.
- **Verificación:** se comprobó que las rutas mencionadas existen en el
  proyecto y que `README.md` explica dónde consultar la skill y las
  conversaciones.
- **Participación:** Adrian Saibol y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/skill-didactica.md`.

### Fase 5. Encargo inicial de la página didáctica

- **Objetivo:** crear una SPA básica, sencilla y comprensible para personas
  sin conocimientos técnicos, utilizando los contenidos de la carpeta
  `contenido/` y ampliándolos con ejemplos cuando fuera necesario.
- **Herramienta:** GitHub Copilot Chat en VS Code.
- **Prompt:** “Crea una página web con los contenidos de la carpeta llamada
  contenidos, ahonda en los temas, busca ejemplos y resúmelos de ser
  necesario; la web debe ser simple y entendible para cualquier persona sin
  conocimientos técnicos, debe ser una SPA básica HTML y CSS”.
- **Resultado:** se planteó una página didáctica de una sola página con
  navegación por secciones y contenidos sobre el código fuente, las fases de
  compilación, la memoria, la depuración, la descompilación y el análisis
  forense.
- **Decisión:** utilizar el contenido de `contenido/pps1_01 proceso
  compilación.md` como base técnica y organizarlo en una experiencia lineal
  de aprendizaje, en lugar de copiar el apunte sin estructura web.
- **Justificación:** una secuencia progresiva permite entender primero el
  código fuente y después sus transformaciones y su ejecución.
- **Verificación:** se comprobó la estructura disponible, se leyó el apunte de
  compilación y se conservó la conversación completa en el archivo de origen.
- **Participación:** integrante responsable del proyecto y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/session-ses_e9b1.md`.

### Fase 6. Implementación de la SPA

- **Objetivo:** convertir el plan de contenidos en una página funcional en
  `index.html`, manteniendo una implementación autocontenida con HTML, CSS y
  JavaScript mínimo para la navegación.
- **Herramienta:** GitHub Copilot Chat en VS Code, en modo de implementación.
- **Prompt:** “Implementa el plan”.
- **Resultado:** se generó la página SPA con secciones navegables, ejemplos de
  código, explicación del flujo de compilación y bloques dedicados a memoria,
  depuración y descompilación.
- **Decisión:** mantener la solución en un único `index.html`, sin añadir
  dependencias ni un framework.
- **Justificación:** el requisito pedía una SPA básica HTML y CSS y el
  contenido no necesitaba una infraestructura de compilación.
- **Verificación:** se revisó el resultado de la implementación dentro de la
  conversación conservada y se relacionó con el archivo final
  `index.html`; las comprobaciones visuales posteriores se documentan en la
  fase siguiente.
- **Participación:** integrante responsable del proyecto y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/session-ses_e9b1.md`.

### Fase 7. Dirección visual y revisión de interfaz

- **Objetivo:** mejorar la claridad visual de la página sin convertirla en una
  plantilla genérica, conectando el diseño con el tema técnico del recorrido
  desde el código hasta la CPU.
- **Herramienta:** skill `frontend-design` y GitHub Copilot Chat en VS Code.
- **Prompt:** “Utiliza la skill `frontend-design` para mejorar la interfaz de
  este proyecto. Analiza la estructura actual, propón una dirección visual
  coherente, conserva la lógica y comprueba la versión móvil y escritorio”.
- **Resultado:** se definió una dirección visual con tipografía monoespaciada,
  contraste oscuro, acento ámbar y una jerarquía basada en etapas del proceso.
  También se revisaron las secciones de viaje, memoria y la vista móvil.
- **Decisión:** aceptar una identidad visual técnica y contenida, con el
  ámbar como señal de ejecución y elementos de navegación por hash, pero
  conservar el contenido y la estructura didáctica.
- **Justificación:** la tipografía y los contrastes evocan el entorno de código
  y ayudan a distinguir conceptos, artefactos y acciones sin añadir
  decoración que distraiga.
- **Verificación:** se realizaron comprobaciones visuales en escritorio y
  móvil mediante capturas de las secciones principales. La conversación
  también detectó un posible comportamiento de desplazamiento al cargar
  fragmentos hash, que debe considerarse si se modifica la navegación.
- **Participación:** integrante responsable del proyecto y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/Conversación_frontend.md` y
  `conversaciones-ia/session-ses_e9b1.md`.

### Fase 8. Documentación y prueba de la skill propia

- **Objetivo:** aplicar la skill propia al material y dejar documentado cómo se
  diseñó, probó y relacionó con las conversaciones anteriores.
- **Herramienta:** skill `proceso-compilacion-didactica`, revisión de
  `SKILL.md` y GitHub Copilot Chat mediante Copilot SDK en VS Code.
- **Prompt:** “En base a esto quiero que desarrolles una skill didáctica
  relacionada con el contenido siguiendo los puntos 3.2 y 3.3”.
- **Resultado:** se definieron pautas para explicar el flujo con entradas y
  salidas, crear actividades observables, diferenciar objeto y ejecutable,
  tratar stack y heap como modelo conceptual y verificar la accesibilidad de
  una web.
- **Decisión:** conservar la skill propia, registrar su prueba y vincularla
  con el contenido y con la página ya creada.
- **Justificación:** la skill convierte las decisiones puntuales del proyecto
  en un procedimiento reutilizable para futuras explicaciones didácticas.
- **Verificación:** se comprobó el frontmatter, la existencia de actividades,
  los límites de precisión y la presencia de evidencia en
  `evidencias/prueba-skill-propia.md`.
- **Participación:** integrante responsable del proyecto y GitHub Copilot Chat.
- **Conversación de origen:** `conversaciones-ia/skill-didactica.md`.

## 3. Inventario de conversaciones originales

Todas las conversaciones disponibles en `conversaciones-ia/` están
referenciadas en este documento y se conservan completas en sus archivos
correspondientes:

| Archivo | Fases relacionadas | Contenido |
|---|---|---|
| `prompt-completo.md` | Fase 1 | Prompt extenso con los apuntes técnicos, el alcance de la página y la estructura del repositorio. |
| `session-ses_e9b1.md` | Fases 5, 6 y 7 | Sesión completa de creación, implementación y revisión de la SPA. |
| `Conversación_frontend.md` | Fase 7 | Uso, instalación, activación y comprobación de la skill pública `frontend-design`. |
| `skill-didactica.md` | Fases 2, 3, 4 y 8 | Creación, prueba y documentación de la skill didáctica propia. |

No se han seleccionado solo las mejores respuestas: el registro enlaza cada
archivo original y describe qué decisiones se tomaron a partir de él.

## 4. Criterios de verificación final

- La skill tiene un `name` estable y una `description` orientada a activación.
- El contenido parte de los apuntes del proyecto y no presenta como universal
  lo que depende de C/C++ o de una arquitectura concreta.
- Las actividades piden decisiones observables y contienen criterio de
  autocorrección.
- Se contemplan accesibilidad, teclado, foco, contraste y alternativas
  textuales si el resultado es una web.
- La skill, la prueba y las decisiones están enlazadas mediante conversaciones
  de origen.
- Los cuatro archivos existentes en `conversaciones-ia/` aparecen en el
  inventario y en al menos una fase concreta.

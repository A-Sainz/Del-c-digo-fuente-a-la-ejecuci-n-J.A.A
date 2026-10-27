# Del código fuente a la ejecución

Material didáctico en formato web sobre el recorrido de un programa desde el
código que escribe una persona hasta las instrucciones que ejecuta la CPU.
Está pensado para personas sin conocimientos técnicos previos y utiliza
explicaciones breves, analogías y ejemplos pequeños en C y lenguaje
ensamblador.

## La web

La experiencia está implementada como una SPA básica en
[`index.html`](./index.html). No requiere servidor, instalación de paquetes ni
proceso de compilación: basta con abrir el archivo en un navegador.

La navegación se organiza en cinco vistas:

1. **Inicio:** presenta la idea central y resume las diez etapas del viaje:
   código fuente, preprocesado, compilación, ensamblado, código objeto,
   enlazado, ejecutable, carga, proceso en memoria y ejecución.
2. **El viaje del código:** explica paso a paso el código fuente, el
   preprocesador de C/C++, el compilador, Assembly, el ensamblador, los
   archivos objeto, el enlazador, los formatos ejecutables y el cargador.
3. **La memoria:** describe las zonas `.text`, `.data`, `.bss`, heap y stack,
   e incluye una comparación entre stack y heap. La explicación aclara que
   este esquema es un modelo conceptual y puede variar según la arquitectura
   y el sistema operativo.
4. **Herramientas:** introduce el depurador, el desensamblador, el
   descompilador y el análisis forense de memoria, incluyendo sus usos y
   limitaciones.
5. **Resumen y glosario:** reúne de nuevo las diez etapas y define los
   términos principales, desde código fuente y compilador hasta proceso,
   memoria y análisis del binario.

Entre los conceptos tratados se encuentran también los formatos **PE**,
**ELF** y **Mach-O**, las arquitecturas **x86-64**, **ARM64** y **RISC-V**, y
el papel de estas herramientas en la depuración, la ingeniería inversa y la
ciberseguridad.

## Características de la interfaz

- Diseño responsive para escritorio y móvil.
- Navegación por botones entre secciones sin recargar la página.
- Menú sticky para mantener las secciones accesibles durante la lectura.
- Ejemplos de código con formato legible y tablas comparativas.
- Estilos autocontenidos en el propio HTML.
- Soporte para navegación inicial mediante hash, por ejemplo
  `index.html#memoria`.
- Foco visible y respeto por `prefers-reduced-motion`.
- Tipografías IBM Plex Sans e IBM Plex Mono cargadas desde Google Fonts
  cuando hay conexión a Internet; el contenido sigue siendo accesible sin
  ellas mediante tipografías alternativas del sistema.

## Uso local

1. Clona o descarga este repositorio.
2. Abre [`index.html`](./index.html) directamente en un navegador.
3. Utiliza el menú superior para cambiar de vista.

No hay comandos `npm`, dependencias externas obligatorias ni backend.

## Estructura del repositorio

```text
.
├── README.md
├── index.html
├── PROCESO.md
├── contenido/
│   ├── 01 - Introducción a los lenguajes de programación.pdf
│   └── pps1_01 proceso compilación.md
├── conversaciones-ia/
│   ├── Conversación_frontend.md
│   ├── prompt-completo.md
│   ├── session-ses_e9b1.md
│   └── skill-didactica.md
├── evidencias/
│   ├── fuentes.md
│   ├── prueba-skill-propia.md
│   └── skill-publica.md
└── skills/
    └── documentar-proceso-conversaciones/
        └── SKILL.md
```

## Documentación y trazabilidad

- [`PROCESO.md`](./PROCESO.md) registra las fases de creación, las
  decisiones, las verificaciones y la participación asociada al proyecto.
- [`contenido/`](./contenido/) conserva los materiales técnicos utilizados
  como base.
- [`conversaciones-ia/`](./conversaciones-ia/) contiene las conversaciones
  originales relacionadas con el diseño, la implementación y la revisión.
- [`evidencias/`](./evidencias/) reúne las comprobaciones y fuentes del
  trabajo.
- [`skills/documentar-proceso-conversaciones/SKILL.md`](./skills/documentar-proceso-conversaciones/SKILL.md)
  define el procedimiento para documentar el proceso con trazabilidad.

## Alcance didáctico

La página explica el flujo habitual de un programa compilado, pero señala
explícitamente los casos que dependen del lenguaje, la arquitectura o el
sistema operativo. En particular:

- El preprocesador se presenta como una fase característica de C/C++, no como
  un paso universal.
- El archivo objeto se distingue del ejecutable final.
- El stack y el heap se explican como un modelo útil, no como una disposición
  idéntica en todas las máquinas.
- Un desensamblador muestra instrucciones de bajo nivel y un descompilador
  solo puede reconstruir de forma aproximada el código original.

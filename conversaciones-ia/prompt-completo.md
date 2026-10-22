Quiero que actúes como un programador web profesional que va crear una página web didáctica con ejemplos prácticos sobre el proceso del código fuente a la ejecución sobre estos apuntes:

1. Introducción
Cuando un programador desarrolla una aplicación utilizando un lenguaje de alto nivel, el código escrito no es directamente comprensible para el procesador. Es necesario realizar una serie de transformaciones hasta obtener instrucciones que la CPU pueda ejecutar.

Por ejemplo, un programador puede escribir:

int resultado = a + b;
Mientras que el procesador trabaja con instrucciones de bajo nivel representadas finalmente mediante código máquina.

El proceso completo comprende varias etapas: preprocesado, compilación, ensamblado, enlazado, carga y ejecución.

2. Código fuente
El código fuente es el conjunto de instrucciones escritas por el programador utilizando un lenguaje de programación.

Por ejemplo:

int main() {
    int a = 10;
    int b = 20;
    int resultado = a + b;

    return 0;
}
Los lenguajes de alto nivel permiten trabajar con conceptos relativamente cercanos a la forma de pensar de las personas, como:

Variables.
Funciones.
Bucles.
Condicionales.
Objetos.
Estructuras de datos.
Operadores.
El procesador no ejecuta directamente estas instrucciones. Deben ser transformadas a instrucciones propias de la arquitectura del procesador.

3. Preprocesador
En algunos lenguajes, especialmente C y C++, existe una fase previa denominada preprocesado.

El preprocesador procesa determinadas directivas antes de que el compilador analice el programa.

Por ejemplo:

#include <stdio.h>

#define MAX 100
La directiva #include permite incorporar el contenido de otros archivos, mientras que #define permite definir macros.

También existen directivas de compilación condicional:

#ifdef DEBUG
    printf("Modo depuración");
#endif
El resultado del preprocesado es un código que posteriormente será analizado por el compilador.

El preprocesador no es una etapa independiente de todos los lenguajes compilados. Es especialmente característico del modelo utilizado por C/C++.

4. Compilador
El compilador es el programa encargado de traducir el código escrito en un lenguaje de alto nivel a una representación de más bajo nivel.

Durante este proceso, el compilador realiza diferentes tareas, entre ellas:

Analizar la sintaxis.
Comprobar determinadas reglas semánticas.
Detectar errores.
Generar código de bajo nivel.
Aplicar optimizaciones.
Generar código adaptado a una determinada arquitectura.
Por ejemplo, una instrucción como:

resultado = a + b;
puede terminar convirtiéndose en varias instrucciones de ensamblador.

El mismo código fuente puede generar diferentes códigos máquina para arquitecturas como x86-64, ARM64 o RISC-V.

5. Lenguaje ensamblador
El lenguaje ensamblador (Assembly) es un lenguaje de bajo nivel muy próximo a las instrucciones que ejecuta el procesador.

Por ejemplo:

mov r0, #1
mov r1, #1
add r2, r0, r1
Las instrucciones y registros disponibles dependen de la arquitectura del procesador.

Algunos conceptos habituales son:

Registros: pequeñas zonas de almacenamiento dentro de la CPU.
Instrucciones: operaciones que puede realizar el procesador.
Direcciones de memoria: posiciones donde se almacenan datos e instrucciones.
Saltos: permiten modificar el flujo de ejecución.
Assembly permite trabajar a un nivel mucho más próximo al hardware que lenguajes como Python, Java o C#.
7. Código objeto
El código generado por el compilador y el ensamblador puede almacenarse en un archivo objeto.

Un archivo objeto puede contener:

Código máquina.
Datos.
Símbolos.
Información de reubicación.
Referencias a funciones o variables externas.
Por ejemplo:

programa.o
Un archivo objeto normalmente todavía no constituye un programa ejecutable completo.

Esto se debe a que un programa puede estar compuesto por varios módulos y utilizar bibliotecas externas.

8. Enlazador
El enlazador o linker se encarga de combinar los diferentes archivos objeto y resolver las referencias entre ellos.

Por ejemplo, un proyecto podría generar:

main.o
utilidades.o
red.o
El enlazador puede combinarlos para generar un ejecutable.

También puede resolver referencias a funciones proporcionadas por bibliotecas.

Por ejemplo, un programa en C puede utilizar:

printf("Hola");
El código de printf no tiene por qué estar incluido directamente en el archivo fuente. El enlazado permite resolver la referencia correspondiente a la biblioteca utilizada.

El resultado final será un archivo ejecutable.
11. Memoria de un proceso
Cuando un programa está ejecutándose, dispone de un espacio de direcciones de memoria.

De forma simplificada, podemos distinguir varias zonas:

Código (.text)
Datos inicializados (.data)
Datos no inicializados (.bss)
Heap
Stack
Esta división es conceptual y la organización exacta depende del sistema operativo, arquitectura y programa.
15. Heap
El heap es una zona de memoria utilizada para la asignación dinámica.

Por ejemplo, en C:

int *numero = malloc(sizeof(int));
se solicita memoria dinámicamente.

En lenguajes que utilizan objetos también encontramos este concepto. Por ejemplo:

Persona persona = new Persona();
La memoria asociada a los objetos se gestiona mediante el sistema de memoria del lenguaje y, habitualmente, interviene el heap.

El tamaño utilizado por el heap puede cambiar durante la ejecución del programa.
17. Stack y Heap
Aunque ambos utilizan memoria durante la ejecución, tienen finalidades diferentes.

Stack	Heap
Relacionado con las llamadas a funciones	Memoria dinámica
Contiene información de ejecución	Permite reservar memoria durante la ejecución
Gestión generalmente automática	Gestión dependiente del lenguaje y entorno
Estructura LIFO	No funciona como una pila de llamadas
Muy utilizado para variables locales y parámetros	Muy utilizado para datos y objetos dinámicos
La representación habitual del stack y el heap como zonas que crecen en direcciones opuestas es un modelo simplificado. No debe considerarse una regla universal para todas las arquitecturas y sistemas operativos.

18. Depurador
Un depurador (debugger) permite analizar el funcionamiento de un programa durante su ejecución.

Entre sus funciones habituales están:

Establecer puntos de ruptura (breakpoints).
Ejecutar el programa paso a paso.
Examinar variables.
Examinar registros.
Inspeccionar la memoria.
Analizar la pila.
Observar las llamadas a funciones.
Detectar errores.
Los depuradores son importantes tanto para el desarrollo de software como para el análisis de programas.
20. Descompilador
Un descompilador intenta realizar una reconstrucción de alto nivel a partir de un programa compilado.

El proceso puede representarse conceptualmente como:

Código máquina → código de alto nivel aproximado
Por ejemplo, puede intentar reconstruir algo parecido a:

int suma(int a, int b) {
    return a + b;
}
Sin embargo, el resultado no tiene por qué coincidir con el código original.

Durante la compilación pueden perderse datos como:

Nombres de variables.
Comentarios.
Nombres originales de algunas funciones.
Estructura exacta del código.
Información de tipos.
Abstracciones utilizadas por el programador.
Además, las optimizaciones pueden modificar considerablemente el código.

Por ello, un descompilador proporciona una reconstrucción aproximada, no una copia del código fuente original.

21. Análisis forense de memoria
El análisis de memoria permite estudiar el contenido de la memoria de un sistema o proceso.

Una herramienta conocida para este propósito es Volatility.

A partir de una captura de memoria se pueden investigar, dependiendo del caso:

Procesos que estaban ejecutándose.
Información de los procesos.
Módulos cargados.
Determinadas estructuras del sistema.
Conexiones y otros artefactos.
Información que puede no estar disponible directamente en el disco.
Esta técnica tiene especial importancia en análisis forense digital y respuesta ante incidentes.

Y por último debes seguir esta estructura repositorio/
├── README.md
├── index.html
├── PROCESO.md
├── conversaciones-ia/
├── evidencias/
│   ├── fuentes.md
│   ├── skill-publica.md
│   └── prueba-skill-propia.md
└── skills/
    └── nombre-skill/
        └── SKILL.md

Este prompt entero quiero que lo guardes en un archivo dentro de conversaciones-ia/

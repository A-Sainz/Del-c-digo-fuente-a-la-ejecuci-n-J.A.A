# Proceso del código fuente a la ejecución

## Flujo general
1. **Código fuente**: el programador escribe instrucciones en alto nivel.
2. **Preprocesado (C/C++)**: expansión de directivas (`#include`, `#define`, `#ifdef`).
3. **Compilación**: análisis, validación semántica básica, optimización y traducción.
4. **Ensamblado**: conversión de assembly a código máquina en objetos (`.o`).
5. **Enlazado**: unión de objetos y bibliotecas para crear el ejecutable.
6. **Carga**: el sistema operativo prepara memoria y recursos.
7. **Ejecución**: la CPU interpreta instrucciones máquina.

## Ejemplo práctico resumido
Código fuente:

```c
int main() {
    int a = 10;
    int b = 20;
    int resultado = a + b;
    return 0;
}
```

Idea de transformación:
- `resultado = a + b;` (alto nivel)
- `add ...` (assembly)
- bytes máquina (ejecución real por CPU)

## Memoria en ejecución
- **.text**: instrucciones
- **.data**: datos inicializados
- **.bss**: datos no inicializados
- **stack**: llamadas/variables locales
- **heap**: memoria dinámica

## Herramientas de análisis
- **Depurador**: inspección en tiempo de ejecución.
- **Descompilador**: reconstrucción aproximada desde binario.
- **Forense de memoria (Volatility)**: análisis de artefactos en memoria.

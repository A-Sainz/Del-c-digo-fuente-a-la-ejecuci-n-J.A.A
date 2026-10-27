---
name: documentar-proceso-conversaciones
description: "Usa esta skill únicamente para documentar en PROCESO.md el trabajo realizado a partir de todas las conversaciones originales guardadas en conversaciones-ia/."
---

# Documentar el proceso con conversaciones de IA

## Propósito

Crear o actualizar `PROCESO.md` utilizando como evidencia las conversaciones
originales de `conversaciones-ia/`. Esta skill solo documenta el proceso: no
crea contenido didáctico, no rediseña la web y no modifica otros archivos salvo
que sea necesario para leer las conversaciones.

## Procedimiento

1. Localiza todos los archivos de `conversaciones-ia/`, incluidos los archivos
   Markdown existentes y los que se hayan añadido durante el trabajo.
2. Lee cada conversación y extrae las fases relevantes, los objetivos, las
   herramientas, los prompts, los resultados, las decisiones y las
   verificaciones.
3. Agrupa la información por fases del trabajo. Una conversación puede
   aparecer en varias fases si contiene decisiones diferentes.
4. Crea `PROCESO.md` si no existe o actualízalo si ya existe. Conserva las
   decisiones válidas que ya estén documentadas y corrige únicamente
   inconsistencias demostrables.
5. Añade al final un inventario de todas las conversaciones originales y las
   fases con las que se relaciona cada archivo.
6. No inventes participantes, prompts, decisiones, resultados o verificaciones.
   Si un dato no aparece en la conversación, escribe: “No consta en la
   conversación conservada”.

## Estructura obligatoria de cada fase

Cada fase relevante debe utilizar exactamente estos campos, en este orden:

- **Objetivo:** qué queríais conseguir.
- **Herramienta:** qué IA utilizasteis y para qué tarea.
- **Prompt:** la instrucción representativa utilizada.
- **Resultado:** qué respuesta o propuesta relevante obtuvisteis.
- **Decisión:** qué aceptasteis, modificasteis o rechazasteis.
- **Justificación:** por qué tomasteis esa decisión.
- **Verificación:** cómo comprobasteis la información o el resultado y qué observasteis.
- **Participación:** qué integrantes participaron en la decisión.
- **Conversación de origen:** nombre del archivo que contiene el intercambio original.

Usa esta plantilla:

```markdown
### Fase [n]. [Título de la fase]

- **Objetivo:** ...
- **Herramienta:** ...
- **Prompt:** ...
- **Resultado:** ...
- **Decisión:** ...
- **Justificación:** ...
- **Verificación:** ...
- **Participación:** ...
- **Conversación de origen:** `conversaciones-ia/nombre-exacto.md`
```

## Reglas de trazabilidad

- El nombre de `Conversación de origen` debe coincidir exactamente con el
  nombre real del archivo.
- Cada archivo de `conversaciones-ia/` debe aparecer al menos una vez en
  `PROCESO.md`.
- Cada fase debe contener los nueve campos obligatorios.
- Los prompts pueden resumirse como instrucciones representativas, pero no
  deben cambiar su intención.
- Los resultados y decisiones deben poder contrastarse con la conversación
  original y con los archivos finales del proyecto.
- Si una conversación no puede leerse completa, registra la limitación en
  `PROCESO.md` y no presentes como completos los datos parciales.
- No copies conversaciones completas dentro de `PROCESO.md`; enlázalas por su
  nombre de archivo y conserva los originales en `conversaciones-ia/`.

## Verificación final

Antes de terminar, comprueba:

1. Que todos los archivos de `conversaciones-ia/` están inventariados.
2. Que cada nombre aparece literalmente en `PROCESO.md`.
3. Que cada fase contiene `Objetivo`, `Herramienta`, `Prompt`, `Resultado`,
   `Decisión`, `Justificación`, `Verificación`, `Participación` y
   `Conversación de origen`.
4. Que no se han atribuido decisiones a personas no identificadas.
5. Que `PROCESO.md` distingue entre información observada en la conversación
   y decisiones tomadas durante la revisión.
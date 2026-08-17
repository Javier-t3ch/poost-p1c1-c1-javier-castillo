# Ficha de trabajo - Clase 2

## Comprensión del problema y alcance

**Asignatura:** Programación Orientada a Objeto Seguro (TI3021)  
**Unidad:** 1  
**Modalidad:** Parejas  
**Tipo de actividad:** Formativa  

| Identificación | Información |
|---|---|
| Integrante 1 | Javier Castillo Galeas |
| Integrante 2 | COMPLETAR |
| Sección y fecha | D-IEC-N2-P1-C1 16-08-2026 |
| URL del repositorio | COMPLETAR AL FINAL |

## Propósito

Analizar y delimitar una funcionalidad antes de diseñar clases o escribir código. La ficha final debe permitir que otra persona comprenda qué necesita el sistema, qué reglas debe respetar y cómo comprobar si responde correctamente.

> **Regla de trabajo:** en esta clase no se diseñan clases, atributos ni métodos. Primero se justifica qué se necesita; la solución técnica comenzará en la Clase 3.

## Situación inicial

> Un entrenador se encuentra con una criatura salvaje cercana e intenta capturarla utilizando una cápsula de su inventario.

## 1. Lectura activa: hechos, dudas y supuestos

### 1.1 Tres hechos explícitos

1. Un entrenador se encuentra con una criatura salvaje cercana
2. el entrenador intenta capturar la criatura
3. El entrenador utiliza una capsula de su inventario para intentar capturar

### 1.2 Tres ambigüedades convertidas en preguntas

| N.º | Expresión ambigua | Pregunta que debe responder el cliente |
|---:|---|---|
| 1 | Cercana | ¿Cuál es la distancia máxima considerada cercana para permitir el intento de captura? |
| 2 | Intenta capturarla | ¿Qué condiciones deben cumplirse para que el intento de captura sea válido? |
| 3 | Capsulas de su inventario | ¿Que debe ocurrir si el entrenador no tiene capsulas disponibles en su inventario? |

### 1.3 Supuesto provisional

**Supuesto:** La captura solo puede intentarse cuando la criatura se encuentra a una distancia máxima de 50 m del entrenador  
**Por qué es provisional:** Porque el enunciado original solo indica que la criatura esta “cercana” y no establece una distancia concreta. El 50 m sacado desde el ppt.   
**Cómo podría confirmarse:** Podría confirmase consultando al cliente. 

Un supuesto no es una verdad del caso. Debe quedar marcado hasta que el cliente, una regla oficial o una evidencia lo confirme.

## 2. Del enunciado a una necesidad clara

Fórmula orientadora:

> Permitir que **[actor]** realice **[acción]** sobre **[elemento]**, bajo **[condición]**, y obtenga **[resultado observable]**.

+
-
--### 2.1 Actor, necesidad y objetivo

**Actor principal:** El entrenador  
**Necesidad:** Capturar una criatura salvaje utilizando una capsula disponible en su inventario.  
**Objetivo reescrito:** Permitir que el entrenador intente capturar una criatura salvaje cuando se encuentre dentro de la distancia permitida y tenga una capsula disponible, aplicando las reglas de captura y entregando un resultado observable de éxito o rechazo.

### 2.2 Entrada, proceso y salida (EPS)

#### Entradas necesarias

1. entrenador
2. Criatura salvaje
3. Distancia entre el entrenador y la criatura
4. Capsula disponible en el inventario

#### Proceso observable

1. Identificar al entrenador que realiza el intento
2. Identificar la criatura que se intenta capturar
3. Verificar si la criatura esta dentro de la distancia permitida
4. Verificar que el entrenador tenga una capsula disponible
5. Aplicar las condiciones conocidas de la captura
6. Informar el resultado al entrenador

#### Salidas esperadas

1. Entrenador identificado
2. Criatura identificada
3. Intento permitido o rechazo por distancia
4. Intento permitido o rechazado por falta de capsula/*

**Prueba de coherencia:** cada salida debe poder explicarse a partir de una entrada, una regla conocida y un paso del proceso.

## 3. Reglas, restricciones y alcance

Una **regla** define qué comportamiento es válido. Una **restricción** limita la solución posible. Un **supuesto** es una condición aceptada temporalmente.

### 3.1 Reglas del problema

1. El intento de captura solo es válido si la criatura se encuentra dentro de la distancia máxima.
2. El entrenador debe disponer de una capsula en su inventario para realizar el intento.
3. Si no se cumple una condición necesaria para la captura, el sistema debe rechazar el intento.
4. El resultado de la captura debe informar si fue exitosa o la causa del rechazo. 

### 3.2 Restricciones

1. Esta primera versión solos enfoca en la funcionalidad de la captura.
2. Solo se con las condiciones y reglas definidas para la primera versión
3. La solución debe poder comprobarse mediante resultados obtenidos, sin depender de información que no haya sido definida.                                                                                                               

### 3.3 Delimitación de la primera versión

#### Dentro del alcance

1. Identificar el entrenador que realiza el intento de captura
2. Verificar que exista una criatura salvaje y una capsula disponible
3. Validar las condiciones conocidas de la captura o informar el resultado

#### Fuera del alcance

1. Estadísticas de vida, ataque, defensas
2. Combate con las criaturas
3. Intercambio, exploración

#### Supuestos por confirmar

1. Distancia máxima para considerar a una criatura “cerca”
2. Condiciones que determinen si una captura tiene éxito
3. Que ocurre con la capsula si la captura es efectiva o fallida. 

### 3.4 Preguntas pendientes

1. Que ocurre con la capsula cuando el intento de captura falla.
2. Que otras condiciones a aparte de la distancia y la disponibilidad de capsula, determina que la captura sea exitosa.

## 4. Criterios de aceptación y revisión entre pares

Un **criterio de aceptación** es una condición concreta y comprobable que permite decidir si una necesidad fue resuelta correctamente.

Estructura sugerida:

> Dado **[contexto]**, cuando **[acción]**, entonces **[resultado observable]**.

**Criterio 1:** Dado que el entrenador tiene una capsula disponible y la criatura se encuentra dentro del rango de distancia definido, cuando se intente la captura, entonces el sistema.
**Criterio 2:** Dado que el entrenador no tiene cápsulas disponibles, cuando intenta capturar una criatura, entonces el sistema impide el intento, no modifica el inventario e informa el motivo.

### 4.1 Intercambio con otra pareja

La pareja revisora debe leer la ficha sin una explicación oral y detectar una ambigüedad que obligaría a inventar una regla al diseñar la solución.

**Pareja revisora:** COMPLETAR  
**Ambigüedad detectada:** COMPLETAR  
**Pregunta sugerida:** COMPLETAR  
**Decisión del equipo:** ACEPTAR / AJUSTAR / RECHAZAR  
**Justificación:** COMPLETAR

## 5. IA como auditora de requisitos

Primero guarden la ficha original. La IA puede detectar vacíos y formular preguntas, pero el equipo conserva la responsabilidad de decidir y justificar cada cambio.

### 5.1 Registro de la consulta

**Herramienta y fecha:** ChatGPT — 16/08/2026  
**Versión original guardada:** SÍ / NO

**Prompt sugerido:**

> Actúa como revisor de requisitos. Analiza esta ficha de captura sin diseñar clases ni escribir código. Detecta ambigüedades o contradicciones; formula cinco preguntas; señala reglas no verificables; no inventes respuestas y marca cada supuesto.

### 5.2 Evaluación de observaciones

| Observación de la IA | Decisión | Justificación del equipo | Cambio realizado |
|---|---|---|---|
| La distancia de “cercana” no está definida. | Aceptar | La clase indica que una regla útil debe ser verificable y presenta 50 m como ejemplo. | “cercana” a “distancia máxima de 50 m, pendiente de confirmación”. |
| No se define qué condiciones determinan una captura exitosa. | Ajustar | Sin esa regla no se puede verificar completamente el resultado. | “captura exitosa” a“resultado de éxito o rechazo; condiciones exactas pendientes”. |
| No se indica qué ocurre si no hay cápsulas. | Aceptar | La ficha necesita contemplar una condición de entrada para evitar inventar comportamiento. | Agregar rechazo sin modificar inventario e informar el motivo. |

### 5.3 Pregunta de autoría

**¿Qué sugerencia rechazaron?** Se rechazó agregar una probabilidad específica de captura, porque esa regla no aparece en el enunciado ni en el material entregado.  
**¿Por qué no correspondía?** Porque habría sido inventar una regla del negocio en lugar de dejarla como pregunta pendiente.  
**¿Qué decisión fue exclusivamente del equipo?** Decidir que las condiciones exactas de éxito de la captura quedan pendientes de confirmación.

> No publiquen contraseñas, correos personales, claves, tokens ni información sensible en la consulta o en el repositorio.

## 6. Mini desafío: cambia una condición

> Cada entrenador puede llevar como máximo seis criaturas activas. Si su equipo está completo, una captura exitosa debe enviarse a la reserva.

### 6.1 Análisis del impacto

**Qué cambió:** Cambio la condición relacionada con la capacidad del equipo: cada entrenador puede llevar como máximo seis criaturas activas, y si el equipo esta completo, una captura exitosa deberá enviarse a la reserva.   
**Secciones afectadas:** ✔ Entrada ✔ Proceso ✔ Salida ✔ Regla ✔ Alcance  
□ Supuesto 
**Nueva decisión:** Incorporar en la interfaz la cantidad de criaturas activa y la reserva, mientras se realiza una captura.   
**Justificación:** El cambio modifica el comportamiento de la captura. Ahora es necesario conocer la cantidad de criaturas activas como entrada y verificar durante el proceso si el equipo está completo para producir una salida diferente según el resultado

### 6.2 Actualización

| Elemento | Antes | Después del cambio |
|---|---|---|
| Entrada/EPS | La captura requiere de la distancia, capsulas y condiciones de captura. | Además, debe verificar si en el equipo hay 6 criaturas para determinar su destino. |
| Proceso | Se valida la captura y se da el resultado | Si la captura es exitosa y el equipo esta completo, la criatura es enviada a reserva |
| Regla | El equipo no puede superar el límite indicado por la nueva condición.  | El entrenador puede tener como máximo 6 criaturas activas, en caso de superar el máximo, la nueva criatura pasa a reserva.  |
| Alcance | Captura de criatura dentro de las condiciones definidas | Se determina el destino de la criatura, si va al equipo o a la reserva.  |

### 6.3 Nuevo criterio de aceptación

**Criterio:** Dado que el entrenador ya tiene seis criaturas en su equipo, cuando se realice una captura exitosa, entonces la nueva criatura no se incorpora al equipo activo y se envía a la reserva.  
**Evidencia esperada:** Se observa que el equipo continúa teniendo como máximo seis criaturas activas y que la criatura capturada aparece en la reserva.

## 7. Ticket de salida

**Resumen en una frase con actor, necesidad, regla principal y resultado:** El entrenador necesita capturar una criatura salvaje si cumple las condiciones de captura, el intento debe respetar las reglas establecidas y, si la captura es exitosa con el equipo completo, la criatura debe enviarse a la reserva.  
**Evidencia más clara:** Un resultado observable en interfaz que indeque el exito o rechazo y cuando el equipo tiene seis criaturas activas, que la captura exitosa termine en la reserva.  
**Ambigüedad pendiente:** Determinar las condiciones exactas que hacen que una captura sea exitosa o fallida.  
**Mejora concreta:** se necesita saber qué condiciones hacen que una captura tenga éxito para poder comprobar si funciona correctamente.

## 8. Comprobación final

- [ ] Conservamos una versión anterior a la auditoría con IA.
- [ ] Actor, necesidad, entradas, proceso y salidas son coherentes.
- [ ] Reglas, restricciones, supuestos y alcance están diferenciados.
- [ ] Los criterios de aceptación son observables y verificables.
- [ ] El cambio del cliente quedó incorporado y justificado.
- [ ] No diseñamos clases ni escribimos código antes de tiempo.

## 9. Entrega

1. Crear un repositorio privado por pareja y agregar al docente como colaborador.
2. Guardar este archivo como `docs/ficha_clase_2.md`.
3. Realizar commits con mensajes claros. Se espera al menos un aporte identificable de cada integrante.
4. Cada estudiante debe pegar el mismo enlace del repositorio en AAI/Intranet e identificar a su pareja.
5. Incluir el identificador del commit final en la entrega.

Convención sugerida para el repositorio:

```text
  poos-p1-c1-portafolio-apellido-nombre
```

Primer flujo Git:

```bash
git clone URL_DEL_REPOSITORIO
cd NOMBRE_DEL_REPOSITORIO
git status
git add docs/ficha_clase_2.md
git commit -m "Completa ficha de alcance de captura"
git push
```

Si existe un bloqueo real de cuenta, autenticación o conectividad, cada integrante debe subir temporalmente la ficha en DOCX o PDF a AAI/Intranet y regularizar el repositorio en la clase siguiente. En esta primera práctica, el dominio técnico de Git no modifica la valoración conceptual de la ficha.

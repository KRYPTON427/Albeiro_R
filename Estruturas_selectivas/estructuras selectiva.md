# Estructuras Selectivas en Programación

Este repositorio explica las **estructuras selectivas** simples, dobles y compuestas. Estas estructuras permiten que un programa tome decisiones basadas en condiciones.

---

##  1. Estructura Selectiva Simple

Permite ejecutar un bloque de instrucciones **solo si** una condición es verdadera.

##  Ejemplo práctico

> **Problema**: Si está oscuro, encender la lámpara.

**Diagrama del ejemplo:**

- Se inicia el proceso.
- Se evalúa la condición: ¿Está oscuro?
- Si la respuesta es "Sí", entonces se ejecuta la acción: encender la lámpara.
- Luego se finaliza el proceso.

---
### Forma general:
<a href=""><img src="https://github.com/KRYPTON427/Albeiro_R/blob/main/Estructura%20simple.png"/></a>

##  ¿Cómo funciona?

- **Inicio**: Punto de partida del flujo.
- **Condición**: Se evalúa una condición lógica.
- **Ejecutar acción**: Si la condición es verdadera, se ejecuta una acción específica.
- **Fin**: El flujo termina sin importar si se cumplió la condición o no.

---

#  Estructura Selectiva Simple

La **estructura selectiva simple** permite ejecutar un bloque de instrucciones **solo si** una condición lógica se evalúa como verdadera. Es una de las estructuras de control más básicas, pero fundamentales en programación.

---

##  Ejemplo práctico

> **Problema:**  
> *Si está oscuro, encender la lámpara.*

###  Descripción del flujo:

1. El proceso inicia.
2. Se evalúa la condición: ¿Está oscuro?
3. Si la condición es verdadera, se ejecuta la acción: **encender la lámpara**.
4. Si la condición es falsa, se ejecuta una acción alternativa: **apagar la lámpara**.
5. El proceso finaliza.

---

##  Forma general

<a href="https://github.com/KRYPTON427/Albeiro_R/blob/main/Estructura%20simple.png">
  <img src="https://github.com/KRYPTON427/Albeiro_R/blob/main/Estructura%20doble.png"/>
</a>

---

##  ¿Cómo funciona?

- **Inicio:**  
  Marca el inicio del flujo.

- **Condición:**  
  Se evalúa una expresión lógica (verdadera o falsa).

- **Si es verdadera:**  
  Se ejecuta la acción principal.

- **Si es falsa:**  
  Se ejecuta una acción alternativa.

- **Fin:**  
  El flujo continúa después de ejecutarse una de las dos opciones.
  
---

# Estructura Selectiva Múltiple

La **estructura selectiva múltiple** permite evaluar una condición que puede tener **varios resultados posibles**, y ejecutar diferentes bloques de instrucciones según el valor obtenido. Es ideal cuando se deben manejar **más de dos alternativas**.

---

##  Ejemplo práctico

> **Problema:**  
> *Dependiendo del día de la semana, realizar una actividad distinta.*

###  Descripción del flujo:

1. El proceso comienza.
2. Se evalúa una variable (por ejemplo: día de la semana).
3. Según el valor, se ejecuta un bloque de instrucciones diferente:
   - Si es lunes → estudiar.
   - Si es martes → entrenar.
   - Si es miércoles → descansar.
   - ...
4. Si no coincide con ninguno, se puede definir un caso por defecto.
5. El proceso finaliza.

---

##  Forma general

<a href="https://github.com/KRYPTON427/Albeiro_R/blob/main/Estrutura%20multiple%20.png">
  <img src="https://github.com/KRYPTON427/Albeiro_R/blob/main/Estrutura%20multiple%20.png" alt="Diagrama Estructura Selectiva Múltiple" />
</a>

---

##  ¿Cómo funciona?

- **Inicio:**  
  Se inicia el flujo del proceso.

- **Evaluar condición:**  
  Se analiza el valor de una variable o expresión.

- **Seleccionar caso:**  
  Se compara el valor con múltiples casos posibles (caso 1, caso 2, ..., caso n).

- **Ejecutar acción según el caso:**  
  Se ejecuta el bloque de instrucciones correspondiente al caso coincidente.

- **Caso por defecto (opcional):**  
  Si ningún caso coincide, se ejecuta un bloque alternativo.

- **Fin:**  
  Finaliza el flujo del proceso.


[Ir a Actividad Operadores Lógicos](Estructuras_selectivas/Actividad_Estructuras_Selectivas.md)

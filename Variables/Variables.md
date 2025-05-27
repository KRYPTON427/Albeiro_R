# Variables y Tipos de datos

Las variables permiten **almacenar datos del programa**. Estas serán de un tipo u otro en función de la información que se guarde en ellas.

```python
nombre = 'Brigithe' # cadena de texto
edad = 30 # número entero
```
El nombre de una variable se conoce como **identificador**, y deberá cumplir las siguientes reglas:

- Comenzar con una letra o un guión bajo.
- El resto del nombre estará formado por letras, números o guiones bajos.
- Los nombres de las variables son *case sensitive*, es decir, no es lo mismo que una variable se llame `resultado` que `RESULTADO`.
- Existen una serie de palabras reservadas que no se pueden utilizar (def, global, return, if, for, ...).
## Resumen de tipos de variables

```python
    edad = 24 # número entero (integer)
    precio = 112.9 # número de punto flotante (float)
    titulo = ‘Aprende Python desde cero’ # cadena de texto (string)
    test = True # booleano
```

## Lectura de datos en Python

La función `input()` permite introducir datos al usuario:

```python
>>> nombre = input()
Leire
>>> print(nombre)
Leire
```

Como se puede ver en el siguiente ejemplo, es posible también mostrar un mensaje al usuario, tal y como muestra el siguiente ejemplo.

```python
>>> nombre = input("Escribe tu nombre: ")
Escribe tu nombre: Leire
>>> print(nombre)
Leire
 ```

## Números
Python soporta dos tipos de números: enteros (integer) y de punto flotante (float).
 
 ```python
# integer
x = 5
print(x)

# float
y = 5.0
print(y)

# Otra forma de declarar un float
z = float(5)
print(z)
```

Si tenemos dudas del valor de una variable, podemos mostrar su tipo utilizando la función `type()`:

```python
>>> x = 5.5
>>> type(x)
<class 'float'>
```

## Cadenas de texto (string)
 Las cadenas de texto o strings se definen mediante comilla simple (`' '`) o doble comilla (`" "`):

```python
mi_nombre = 'Ane'
print(mi_nombre)
mi_nombre= "Ane"
print(mi_nombre)
```

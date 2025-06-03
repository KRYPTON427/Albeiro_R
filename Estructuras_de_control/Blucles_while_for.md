## Bucles
Los bucles permiten ejecutar un bloque de código tantas veces como queramos. 

# Sentencia WHILE

La sentencia `while` permite ejecutar un bloque de código mientras la expresión que definamos se cumpla (es decir, devuelva `True`). Python interpretará como `True` cualquier valor distinto a `0` o `None`.

```python
contador = 0
while(contador < 5):
    # Se ejecutará mientras la variable contador sea menor a 5.
    contador = contador+1
    print("Iteración número",contador)
print ("¡Fin!")
```

Para detener una ejecución de forma voluntaria se utiliza la sentencia `break`:
   
```python 
contador = 0
while(contador < 5):
    contador = contador+1
    print("Iteración número",contador)
    if contador == 3:
        break
print ("¡Fin!")
```

También es posible saltar únicamente la iteración actual mediante la sentencia `continue`:

```python
contador = 0
while(contador < 5):
    contador = contador+1
    if contador == 3:
        continue
    print("Iteración número {}".format(contador))
print ("¡Fin!")
```

La salida del programa anterior será la siguiente:
```
    Iteración número 1
    Iteración número 2
    Iteración número 4
    Iteración número 5
    Bucle while finalizado
```

Otros lenguajes de programación ofrecen otra estructura similar conocida como `DO - WHILE`. No es el caso de Python, por lo que habría que emular dicho comportamiento mediante nuestro código.

#### Bucle WHILE con ELSE

La expresión `else` puede utilizarse también tras un bloque `while`. De este forma podemos definir un bloque de código que se ejecutará una vez finalizado el bloque `while` (es decir, cuando la condición se evalúe `False` y no se haya finalizado mediante un `break`):

```python
count = 0
while(count < 5):
    count = count+1
    print("Iteración número {}".format(count))
else:
    print("Bucle while finalizado")
 ```   
# Sentencia FOR
A diferencia de otros lenguajes de programación, en Python la sentencia FOR itera únicamente por secuencias (listas, tuplas, cadenas de caracteres,...).

```python
alumnos = ["Ane", "Mikel", "Unai", "Lorea"]
for alumno in alumnos:
    print(alumno)
```

También es posible utilizarlo para recorrer un string:

```python
frase = "Aprendiendo Python"
for c in frase:
    print(c)
```

Para detener una ejecución se utiliza la sentencia `break`:

```python
numeros = [4,8,2,7,1,9,3,5]
total = 0

for n in numeros:
    total += n
    if total > 10
        break
```

Al igual que en otras estructuras de repetición, también es posible saltar únicamente la iteración actual mediante la sentencia `continue`:

```python
numeros = [4,8,2,7,1,9,3,5]
total = 0

# solo sumar los números impares
for num in numeros:
    if num % 2 == 0:
        print("Numero par, no lo sumamos")
        continue
    total += n
```

#### Bucle FOR con ELSE
Python permite definir un bloque de código que se ejecutará una vez finalice la iteración por todos los elementos de una lista. Es importante mencionar que no se ejecutará si se ha finalizado mediante `break`.

```python
alumnos = ["Ane", "Mikel", "Unai", "Lorea"]
for alumno in alumnos:
    print(alumno)
else:
    print("No quedan más alumnos.")
```

#### La función range()

La función `range([start,]  stop  [,  step])` devuelve una secuencia de números. Es por ello que se utiliza de forma frecuente para iterar:

```python
for i in range(3):
    print(i)
# 0
# 1
# 2
```

También podemos indicar el inicio, fin y step:

```python
print("Números del 5 al 10") 
for i in range(5,  10): 
    print(i,  end=', ')
# 5,  6,  7,  8,  9,

print("Números impares del 1 al 10")
for i in range(1,  10,  2):
    print(i,  end=', ')
# 1,  3,  5,  7,  9,
```

Para iterar por una lista utilizando el índice, basta con combinarlo con la función `len()`:

```python
    alumnos = ["Ane", "Mikel", "Unai", "Lorea"]
    for i in range(len(alumnos)):
    	print(alumnos[i])
```

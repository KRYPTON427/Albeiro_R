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

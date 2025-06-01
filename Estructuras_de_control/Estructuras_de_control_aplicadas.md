# Estructuras de control

## Condicionales
Las estructuras de control se utilizan para **ejecutar bloques de código en función de condiciones**.

### Sentencia IF - ELSE
Se evalúa la condición especificada en la sentencia `if` y en caso de cumplirse se ejecutará el bloque de código indentado (tabulado). En caso de que el resultado de la condición sea `False`, el bloque especificado no se ejecutará:

```python
temperatura = 18  # Temperatura en grados en Bogotá
if temperatura < 20:
    print("Hace frío, mejor llevar chaqueta")
```

Las condiciones pueden tener mayor complejidad:

```python
edad = 12
altura_cm = 135
if edad >= 10 and altura_cm >= 130:
    print("Puede ingresar al parque sin acompañante")
```


Mediante la palabra reservada `else` es posible especificar un bloque de código que se ejecute en caso de que la condición no se cumpla:

```python
bicicleta_prestada = False
if bicicleta_prestada:
    print("Llévala con cuidado por los cerros")
else:
    print("No puedes salir al ciclopaseo sin bicicleta")
```

También podemos comprobar más condiciones mediante la expresión `elif`. En este caso, se seguirán comprobando todas las condiciones `elif` hasta que una de ellas se cumpla. En caso contrario, se ejecutará el bloque de código dentro de `else` (si lo hubiera).

```python
hora = 7
if hora < 6:
    print("Muy temprano para ir al colegio")
elif hora < 8:
    print("Hora de alistarse para clase en el colegio")
else:
    print("Ya es tarde, toca correr a la estación de TransMiCable")
```

Tal y como muestra el siguiente código de ejemplo, Python no tiene limitaciones para anidar distintos bloques de `IF`s.

```python
pico_y_placa = True
es_moto = False

if pico_y_placa:
    if es_moto:
        print("Puedes circular, las motos no tienen pico y placa")
    else:
        print("Debes dejar el carro en casa hoy")
else:
    print("Hoy puedes salir con el vehículo")

```

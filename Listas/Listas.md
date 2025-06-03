# Listas y tuplas

Las listas permiten **guardar más de un elemento** dentro de una variable, y además hacerlo en un orden concreto. Pueden contener un número **ilimitado** de elementos de **cualquier tipo**:

```python
    # Lista vacía
    lista_vacia = []

    # Lista con valores
    alumnos = ["Daniela", "Davil", "Felipe", "Karen"]
    
    # Acceder a elementos
    print(alumnos[0]) # muestra "Daniela"
    print(alumnos[1]) # muestra "Davil"
    print(alumnos[2]) # muestra "Felipe"
    print(alumnos[-1]) # muestra "Keren"
    
    # Cambiar un elemento
    alumnos[0] = "Nora" 
```

Los **métodos más utilizados** con las listas son los siguientes:
| Método | Acción |
|--|--|
| `alumnos.append("Amaia")` | Inserta "Jon" al final de la lista |
| `alumnos.insert(0,"Amaia")` | Inserta "Amaia" en la posición 0 |
| `alumnos.remove("Amaia")` | Elimina la primera aparición de "Amaia" de la lista |
| `alumnos.pop()` | Elimina el último elemento de la lista |
| `alumnos.pop(3)` | Elimina el cuarto elemento de la lista |
| `alumnos.clear()` | Elimina todos los elementos de la lista |
| `alumnos.index("Amaia")` | Devuelve el índice de la primera aparición de "Amaia" |
| `alumnos.sort()` | Ordena la lista (los elementos deben ser comparables) |
| `sorted(alumnos)` | Devuelve una copia de la lista 'alumnos' ordenada (no ordena la pasada como parámetro)  |
| `alumnos.reverse()` | Ordena la lista en orden inverso |
| `alumnos.copy()` | Devuelve una copia de la lista |
| `alumnos.extend(otra_lista)` | Fusiona las dos listas |

### Acceder a varios elementos de una lista

Si queremos acceder a un subconjunto de elementos de la lista, es posible hacerlo de la siguiente manera:

```python
lista = ['a','b','c','d','e','f']
# Elementos de la segunda a la cuarta posición
print(lista[1:3]) # Salida: ['b', 'c']

# Elementos desde la primera hasta la cuarta posición
print(lista[:3]) # Salida: ['a', 'b', 'c']

# Elementos desde la tercera posición hasta el final
print(lista[2:]) # Salida: ['c', 'd', 'e', 'f']
```

### Recorrer una lista
La forma habitual de recorrer una lista es mediante la sentencia `for`, tal y como muestra el ejemplo a continuación:

```python
    for elemento in ['Python','JavaScript','JAVA']:
        print("Programo en ", elemento)
```
De igual manera se podría hacer mediante la sentencia `while`:

```python
    lista =  ['Python','JavaScript','JAVA']
    i = 0
    sizeofList = len(lista) 
    while i < sizeofList :
        print(lista[i]) 
        i += 1
```


## Tuplas
Las tuplas son **listas inmutables**. Es decir, una vez declaradas, no se pueden realizar modificaciones sobre ellas (añadir/eliminar elementos o hacer modificaciones sobre ellos). Para definir una tupla se escriben los elementos entre paréntesis:

```python
    valores = (1,2,3,4,5)
    print(valores)  # Salida: (1, 2, 3, 4, 5) 
    
    # tuple with mixed datatypes
    valores_mixtos = (1, "Hola", 2.5, False)
    print(valores_mixtos)  # Salida: (1, 'Hola', 2.5, False)
```
El acceso a sus elementos se hace de igual que con listas:

```python
    valores = ("a", "b", "c","d","e","f")  
    print(valores[1]) # Salida: 'b'
    print(valores[2:4]) # Salida: ('c', 'd')
```

Una acción típica de las tuplas es "desempaquetar" (unpack) sus valores, es decir, asignarlos a variables directamente:

```python
    tupla = (1, "Hola", 2.5) # Creamos la tupla
    
    var1, var2, var3 = tupla # Hacemos el unpack
    
    print(var1)      # 1
    print(var2)      # 'Hola' 
    print(var3)      # 2.5
```
[Ir a Actividad Listas y Tuplas](./actividad_Listas_tuplas.md)

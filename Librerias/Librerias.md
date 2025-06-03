# Librerías Populares en Python

## ¿Qué es una librería?
Una librería es un conjunto de módulos ya desarrollados por otros que puedes reutilizar. Muchas librerías populares en Python te permiten realizar tareas comunes como análisis de datos, visualización, machine learning, manejo de archivos, etc.

Estas librerías se importan de manera similar a los módulos definidos por el usuario.

---
# Instalación de librerías

Algunas librerías no están incluidas en la instalación estándar de Python, por lo que es necesario instalarlas utilizando pip:

bash
```
pip install numpy
pip install pandas
```
## Cómo importar una librería

### Importación básica
```python
import numpy
```

### Con alias (recomendado para simplificar código)

```python
import numpy as np
```

### Importar solo funciones específicas

```python
from math import sqrt, pi
```

### Importar todo (no recomendado)

```python
from math import *
```

---

##  Ejemplo Práctico Usando Librerías Populares

```python
# Librerías para análisis y visualización
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Librería para HTTP
import requests

# Librería para machine learning
from sklearn.linear_model import LinearRegression

# Librería para manejo de fechas
import datetime

# Librería para trabajar con rutas de archivo
from pathlib import Path
```

---

[Ir a Actividad Librerias](./Actividad_Librerias.md)


# Revisión de Python Básico

## Tabla de Contenidos

1. [Variables y Tipos de Datos](#variables-y-tipos-de-datos)
2. [Operadores](#operadores)
3. [Estructuras de Control](#estructuras-de-control)
4. [Listas y Diccionarios](#listas-y-diccionarios)
5. [Funciones](#funciones)
6. [Módulos y Librerías](#módulos-y-librerías)
7. [Manejo de Archivos](#manejo-de-archivos)
8. [Excepciones](#excepciones)
9. [Programación Orientada a Objetos (POO)](#programación-orientada-a-objetos)
10. [List Comprehensions](#list-comprehensions)
11. [Ejercicios Prácticos](#ejercicios-prácticos)

---

## Variables y Tipos de Datos

### Tipos Básicos

Python es un lenguaje de tipado dinámico. No necesitas declarar el tipo de variable explícitamente.

```python
# Enteros
edad = 25
temperatura = -10

# Flotantes
precio = 19.99
pi = 3.14159

# Cadenas de texto (strings)
nombre = "Miguel"
mensaje = 'Hola mundo'
nota = """Este es un
texto multilínea"""

# Booleanos
es_verdadero = True
es_falso = False

# None (valor nulo)
valor = None
```

### Conversión de Tipos

```python
# Convertir a entero
numero = int("42")        # 42
numero = int(3.14)        # 3 (trunca el decimal)

# Convertir a flotante
decimal = float("3.14")   # 3.14
decimal = float(42)       # 42.0

# Convertir a cadena
texto = str(42)           # "42"
texto = str(3.14)         # "3.14"

# Convertir a booleano
bool(1)                   # True
bool(0)                   # False
bool("")                  # False (cadena vacía)
bool("texto")             # True (cadena no vacía)
```

### Operaciones con Strings

```python
nombre = "Python"
version = "3.11"

# Concatenación
mensaje = nombre + " " + version  # "Python 3.11"

# Formateo de strings (f-strings, recomendado)
mensaje = f"{nombre} {version}"   # "Python 3.11"
precio = 19.99
info = f"El precio es ${precio:.2f}"  # "El precio es $19.99"

# Formateo con .format()
mensaje = "{} {}".format(nombre, version)

# Métodos útiles
texto = "  hola mundo  "
texto.strip()             # "hola mundo" (elimina espacios)
texto.upper()             # "  HOLA MUNDO  "
texto.lower()             # "  hola mundo  "
texto.replace("mundo", "Python")  # "  hola Python  "

# Acceso a caracteres
palabra = "Python"
palabra[0]                # 'P' (primer carácter)
palabra[-1]               # 'n' (último carácter)
palabra[0:3]              # 'Pyt' (slicing)
```

---

## Operadores

### Operadores Aritméticos

```python
a = 10
b = 3

a + b    # 13 (suma)
a - b    # 7 (resta)
a * b    # 30 (multiplicación)
a / b    # 3.333... (división)
a // b   # 3 (división entera)
a % b    # 1 (módulo, resto de la división)
a ** b   # 1000 (potencia)
```

### Operadores de Comparación

```python
a = 5
b = 10

a == b   # False (igualdad)
a != b   # True (desigualdad)
a < b    # True (menor que)
a > b    # False (mayor que)
a <= b   # True (menor o igual)
a >= b   # False (mayor o igual)
```

### Operadores Lógicos

```python
x = True
y = False

x and y  # False (AND lógico)
x or y   # True (OR lógico)
not x    # False (NOT lógico)
```

### Operadores de Asignación

```python
x = 10
x += 5   # x = x + 5 → 15
x -= 3   # x = x - 3 → 12
x *= 2   # x = x * 2 → 24
x /= 4   # x = x / 4 → 6.0
x //= 2  # x = x // 2 → 3
x **= 2  # x = x ** 2 → 9
```

---

## Estructuras de Control

### Condicionales (if/elif/else)

```python
edad = 18

if edad >= 18:
    print("Es mayor de edad")
elif edad >= 13:
    print("Es adolescente")
else:
    print("Es menor de edad")

# Operador ternario
mensaje = "Mayor" if edad >= 18 else "Menor"
```

### Bucles (for y while)

#### Bucle for

```python
# Iterar sobre una lista
frutas = ["manzana", "banana", "naranja"]
for fruta in frutas:
    print(fruta)

# Iterar sobre un rango
for i in range(5):        # 0, 1, 2, 3, 4
    print(i)

for i in range(2, 10):    # 2, 3, 4, 5, 6, 7, 8, 9
    print(i)

for i in range(0, 10, 2): # 0, 2, 4, 6, 8 (paso de 2)
    print(i)

# Iterar con índice
for i, fruta in enumerate(frutas):
    print(f"{i}: {fruta}")
```

#### Bucle while

```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1

# Bucle infinito con break
while True:
    entrada = input("Ingresa 'salir' para terminar: ")
    if entrada == "salir":
        break
    print(f"Recibido: {entrada}")
```

#### Control de flujo: break y continue

```python
# break: sale del bucle
for i in range(10):
    if i == 5:
        break
    print(i)  # Imprime 0, 1, 2, 3, 4

# continue: salta a la siguiente iteración
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # Imprime 1, 3, 5, 7, 9
```

---

## Listas y Diccionarios

### Listas

Las listas son colecciones ordenadas y mutables de elementos.

```python
# Crear listas
numeros = [1, 2, 3, 4, 5]
frutas = ["manzana", "banana", "naranja"]
mixta = [1, "texto", 3.14, True]
vacia = []

# Acceso a elementos
frutas[0]              # "manzana" (primer elemento)
frutas[-1]             # "naranja" (último elemento)
frutas[1:3]            # ["banana", "naranja"] (slicing)

# Modificar elementos
frutas[0] = "pera"     # Modifica el primer elemento

# Agregar elementos
frutas.append("uva")           # Agrega al final
frutas.insert(1, "kiwi")       # Inserta en posición 1
frutas.extend(["mango", "papaya"])  # Agrega múltiples elementos

# Eliminar elementos
frutas.remove("banana")        # Elimina por valor
frutas.pop()                   # Elimina y retorna el último
frutas.pop(0)                  # Elimina y retorna el índice 0
del frutas[1]                  # Elimina por índice

# Métodos útiles
len(frutas)                    # Longitud de la lista
frutas.count("manzana")        # Cuenta ocurrencias
frutas.index("naranja")       # Índice del elemento
frutas.sort()                  # Ordena la lista (modifica in-place)
sorted(frutas)                 # Retorna lista ordenada (no modifica)
frutas.reverse()               # Invierte la lista
```

### Tuplas

Las tuplas son inmutables (no se pueden modificar después de crearlas).

```python
# Crear tuplas
coordenadas = (10, 20)
punto = 10, 20  # También válido
color = ("rojo", "verde", "azul")

# Acceso (igual que listas)
coordenadas[0]  # 10

# Desempaquetado
x, y = coordenadas  # x = 10, y = 20
```

### Diccionarios

Los diccionarios almacenan pares clave-valor.

```python
# Crear diccionarios
persona = {
    "nombre": "Miguel",
    "edad": 30,
    "ciudad": "Arequipa"
}

# Acceso a valores
persona["nombre"]              # "Miguel"
persona.get("nombre")          # "Miguel"
persona.get("email", "N/A")    # "N/A" (valor por defecto si no existe)

# Modificar y agregar
persona["edad"] = 31           # Modifica valor existente
persona["email"] = "miguel@example.com"  # Agrega nueva clave

# Eliminar
del persona["ciudad"]          # Elimina clave-valor
valor = persona.pop("edad")    # Elimina y retorna el valor

# Métodos útiles
persona.keys()                 # Todas las claves
persona.values()               # Todos los valores
persona.items()                # Pares (clave, valor)

# Iterar sobre diccionario
for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

### Conjuntos (Sets)

Los conjuntos almacenan elementos únicos (sin duplicados).

```python
# Crear conjuntos
numeros = {1, 2, 3, 4, 5}
frutas = set(["manzana", "banana", "naranja"])

# Operaciones
numeros.add(6)                 # Agregar elemento
numeros.remove(5)              # Eliminar elemento
numeros.discard(10)            # Eliminar si existe (no da error)

# Operaciones de conjuntos
a = {1, 2, 3}
b = {3, 4, 5}
a.union(b)                     # {1, 2, 3, 4, 5}
a.intersection(b)              # {3}
a.difference(b)                # {1, 2}
```

---

## Funciones

### Definir Funciones

```python
# Función simple
def saludar():
    print("¡Hola!")

# Función con parámetros
def saludar_nombre(nombre):
    print(f"¡Hola, {nombre}!")

# Función con valor por defecto
def saludar_completo(nombre, mensaje="Bienvenido"):
    print(f"{mensaje}, {nombre}!")

# Función con retorno
def sumar(a, b):
    return a + b

resultado = sumar(5, 3)  # 8

# Función con múltiples retornos
def dividir(a, b):
    cociente = a // b
    resto = a % b
    return cociente, resto

coc, res = dividir(10, 3)  # coc = 3, res = 1
```

### Argumentos Posicionales y por Nombre

```python
def calcular_area(base, altura):
    return base * altura

# Argumentos posicionales
area = calcular_area(5, 10)  # 50

# Argumentos por nombre
area = calcular_area(altura=10, base=5)  # 50

# Mezcla (posicionales primero, luego por nombre)
area = calcular_area(5, altura=10)  # 50
```

### Argumentos Arbitrarios

```python
# *args: argumentos posicionales arbitrarios
def sumar_todos(*numeros):
    total = 0
    for num in numeros:
        total += num
    return total

sumar_todos(1, 2, 3, 4)  # 10

# **kwargs: argumentos por nombre arbitrarios
def mostrar_info(**datos):
    for clave, valor in datos.items():
        print(f"{clave}: {valor}")

mostrar_info(nombre="Miguel", edad=30, ciudad="Arequipa")
```

### Funciones Lambda

Funciones anónimas de una sola línea.

```python
# Función lambda simple
cuadrado = lambda x: x ** 2
cuadrado(5)  # 25

# Usar con funciones de orden superior
numeros = [1, 2, 3, 4, 5]
cuadrados = list(map(lambda x: x ** 2, numeros))  # [1, 4, 9, 16, 25]
pares = list(filter(lambda x: x % 2 == 0, numeros))  # [2, 4]
```

---

## Módulos y Librerías

### Importar Módulos

```python
# Importar módulo completo
import math
math.sqrt(16)  # 4.0

# Importar con alias
import numpy as np
np.array([1, 2, 3])

# Importar funciones específicas
from math import sqrt, pi
sqrt(16)  # 4.0

# Importar todo (no recomendado)
from math import *
```

### Crear tu Propio Módulo

**mi_modulo.py:**
```python
def mi_funcion():
    return "Hola desde mi módulo"

PI = 3.14159
```

**otro_archivo.py:**
```python
import mi_modulo
mi_modulo.mi_funcion()
print(mi_modulo.PI)
```

### Librerías Comunes para ML

```python
import numpy as np          # Arrays y operaciones numéricas
import pandas as pd         # DataFrames y análisis de datos
import matplotlib.pyplot as plt  # Visualización
import sklearn             # Machine Learning
```

---

## Manejo de Archivos

### Leer Archivos

```python
# Leer archivo completo
with open("archivo.txt", "r") as archivo:
    contenido = archivo.read()

# Leer línea por línea
with open("archivo.txt", "r") as archivo:
    for linea in archivo:
        print(linea.strip())  # strip() elimina \n

# Leer todas las líneas en una lista
with open("archivo.txt", "r") as archivo:
    lineas = archivo.readlines()
```

### Escribir Archivos

```python
# Escribir archivo
with open("archivo.txt", "w") as archivo:
    archivo.write("Primera línea\n")
    archivo.write("Segunda línea\n")

# Agregar al final del archivo
with open("archivo.txt", "a") as archivo:
    archivo.write("Tercera línea\n")
```

### Modos de Apertura

- `"r"`: Lectura (por defecto)
- `"w"`: Escritura (sobrescribe si existe)
- `"a"`: Append (agregar al final)
- `"x"`: Crear (falla si existe)
- `"b"`: Modo binario (ej: `"rb"`, `"wb"`)

### CSV

```python
import csv

# Leer CSV
with open("datos.csv", "r") as archivo:
    lector = csv.reader(archivo)
    for fila in lector:
        print(fila)

# Escribir CSV
with open("datos.csv", "w", newline="") as archivo:
    escritor = csv.writer(archivo)
    escritor.writerow(["Nombre", "Edad", "Ciudad"])
    escritor.writerow(["Miguel", 30, "Arequipa"])
```

---

## Excepciones

### try/except

```python
# Manejo básico de excepciones
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Error: División por cero")

# Múltiples excepciones
try:
    numero = int(input("Ingresa un número: "))
    resultado = 10 / numero
except ValueError:
    print("Error: Debes ingresar un número válido")
except ZeroDivisionError:
    print("Error: No puedes dividir por cero")
except Exception as e:
    print(f"Error inesperado: {e}")
```

### else y finally

```python
try:
    archivo = open("datos.txt", "r")
    contenido = archivo.read()
except FileNotFoundError:
    print("El archivo no existe")
else:
    # Se ejecuta si no hay excepciones
    print("Archivo leído correctamente")
finally:
    # Siempre se ejecuta
    print("Limpiando recursos")
```

### raise (Lanzar Excepciones)

```python
def dividir(a, b):
    if b == 0:
        raise ValueError("No se puede dividir por cero")
    return a / b
```

---

## Programación Orientada a Objetos

### Clases y Objetos

```python
class Persona:
    # Atributo de clase
    especie = "Homo sapiens"

    # Constructor
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    # Método de instancia
    def presentarse(self):
        return f"Soy {self.nombre} y tengo {self.edad} años"

    # Método estático
    @staticmethod
    def es_adulto(edad):
        return edad >= 18

    # Método de clase
    @classmethod
    def desde_ano_nacimiento(cls, nombre, ano_nacimiento):
        edad = 2024 - ano_nacimiento
        return cls(nombre, edad)

# Crear instancia
persona1 = Persona("Miguel", 30)
print(persona1.presentarse())

# Usar método estático
print(Persona.es_adulto(25))  # True

# Usar método de clase
persona2 = Persona.desde_ano_nacimiento("Ana", 1995)
```

### Herencia

```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hacer_sonido(self):
        return "Hace un sonido"

class Perro(Animal):
    def hacer_sonido(self):
        return "Guau!"

    def ladrar(self):
        return f"{self.nombre} está ladrando"

perro = Perro("Fido")
print(perro.hacer_sonido())  # "Guau!"
print(perro.ladrar())        # "Fido está ladrando"
```

### Encapsulación

```python
class CuentaBancaria:
    def __init__(self, saldo_inicial):
        self._saldo = saldo_inicial  # Protegido (convención)
        self.__pin = "1234"          # Privado (name mangling)

    def depositar(self, cantidad):
        if cantidad > 0:
            self._saldo += cantidad

    def obtener_saldo(self):
        return self._saldo

cuenta = CuentaBancaria(1000)
cuenta.depositar(500)
print(cuenta.obtener_saldo())  # 1500
```

---

## List Comprehensions

Forma concisa de crear listas.

```python
# Forma tradicional
cuadrados = []
for i in range(10):
    cuadrados.append(i ** 2)

# List comprehension
cuadrados = [i ** 2 for i in range(10)]

# Con condición
pares = [i for i in range(20) if i % 2 == 0]

# Anidado
matriz = [[i * j for j in range(3)] for i in range(3)]
# [[0, 0, 0], [0, 1, 2], [0, 2, 4]]

# Dictionary comprehension
cuadrados_dict = {i: i ** 2 for i in range(5)}
# {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

# Set comprehension
cuadrados_set = {i ** 2 for i in range(5)}
# {0, 1, 4, 9, 16}
```

---

## Ejercicios Prácticos

### Ejercicio 1: Calculadora Simple

Escribe una función que reciba dos números y una operación (+, -, *, /) y retorne el resultado.

```python
def calculadora(a, b, operacion):
    # Tu código aquí
    pass
```

### Ejercicio 2: Contador de Palabras

Escribe una función que reciba un texto y retorne un diccionario con la frecuencia de cada palabra.

```python
def contar_palabras(texto):
    # Tu código aquí
    pass
```

### Ejercicio 3: Filtrar Lista

Escribe una función que reciba una lista de números y retorne solo los números pares mayores a 10.

```python
def filtrar_numeros(numeros):
    # Tu código aquí
    pass
```

### Ejercicio 4: Clase Calculadora

Crea una clase `Calculadora` con métodos para sumar, restar, multiplicar y dividir, que mantenga un historial de operaciones.

```python
class Calculadora:
    # Tu código aquí
    pass
```

### Ejercicio 5: Leer y Procesar CSV

Escribe un script que lea un archivo CSV y calcule el promedio de una columna numérica.

```python
# Tu código aquí
```

---

## Recursos Adicionales

- [Documentación oficial de Python](https://docs.python.org/es/3/)
- [Python Tutorial (oficial)](https://docs.python.org/es/3/tutorial/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)

---

**¡Buena suerte con tu aprendizaje de Python!** 🐍


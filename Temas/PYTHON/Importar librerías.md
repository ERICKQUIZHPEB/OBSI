En Python, para utilizar funcionalidades adicionales más allá de las que vienen incluidas en la biblioteca estándar, es necesario importar librerías externas. Las librerías son colecciones de módulos y funciones que extienden las capacidades del lenguaje y permiten realizar tareas específicas de manera más eficiente. Para importar una librería en Python, se utiliza la instrucción `import`. Aquí te muestro algunos ejemplos de cómo importar librerías comunes: 
1. **Importar toda la librería:** 
Si deseas importar toda la librería, puedes usar la siguiente sintaxis:

```python

import nombre_libreria
```
Por ejemplo, para importar la librería `math`, que proporciona funciones matemáticas, puedes hacer lo siguiente:

```python
import math
```
Luego, puedes utilizar las funciones y constantes de la librería `math` utilizando la notación de punto, como `math.sqrt()` para obtener la raíz cuadrada de un número. 
2. **Importar la librería con un alias:** 
Puedes darle un alias a la librería para abreviar su nombre y facilitar su uso:

```python
import nombre_libreria as alias
```
Por ejemplo, para importar `pandas` con el alias `pd`, una librería popular para el análisis de datos, puedes hacer lo siguiente:

```python
import pandas as pd
```
Luego, puedes utilizar las funciones y objetos de `pandas` usando `pd` en lugar de `pandas`. 
3. **Importar una función o módulo específico de la librería:** 
Si solo necesitas una función o un módulo específico de una librería, puedes importar solo eso para ahorrar memoria y tiempo de carga:

```python
from nombre_libreria import funcion_o_modulo
```
Por ejemplo, si solo necesitas la función `sin()` de la librería `math`, puedes hacer lo siguiente:

```python
from math import sin
```
Luego, puedes utilizar directamente `sin()` sin tener que anteponer `math`.

Recuerda que antes de usar una librería, esta debe estar instalada en tu entorno de Python. Puedes instalar librerías utilizando herramientas como `pip`. Por ejemplo, para instalar la librería `pandas`, puedes ejecutar el siguiente comando en la terminal o símbolo del sistema:

```

pip install pandas
```



Una vez que hayas importado una librería, puedes aprovechar sus funciones y capacidades para realizar tareas más complejas y avanzadas en tu código de Python.

**Ejercicio 7
```python
import random
def jugar_loteria():

    # Números para el sorteo
    numeros_ganadores = random.sample(range(1, 6), 2)
    numeros_ganadores.sort()

    # Pedir al jugador que elija sus números

    print("Bienvenido/a al juego de lotería.")

    print("Elige 2 números entre 1 y 5:")

    numeros_elegidos = []

    for i in range(2):

        while True:

            try:

                numero = int(input(f"Ingrese el número {i+1}: "))

                if 1 <= numero <= 5 and numero not in numeros_elegidos:

                    numeros_elegidos.append(numero)

                    break

                else:

                    print("Número inválido o repetido. Intente nuevamente.")

            except ValueError:

                print("Entrada inválida. Intente nuevamente.")
    numeros_elegidos.sort()

    # Mostrar resultados

    print("\nNúmeros ganadores:", numeros_ganadores)

    print("Tus números elegidos:", numeros_elegidos)

    # Comparar los números del jugador con los números ganadores

    numeros_acertados = set(numeros_ganadores) & set(numeros_elegidos)

    aciertos = len(numeros_acertados)


    if aciertos == 2:

        print("¡Felicidades! Ganaste el premio mayor tuviste 2 aciertos.")

    elif aciertos >= 1:

        print(f"¡Ganaste un boleto! Tuviste {aciertos} aciertos.")

    else:

        print("Lo siento, no ganaste. Inténtalo de nuevo.")

# Ejecutar el juego

jugar_loteria()
```

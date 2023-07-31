# Python
Python es un lenguaje de programación de alto nivel, interpretado, versátil y fácil de aprender.

**Ejercicio 1
```python
print('Hello work')
``` 

**Ejercicio 2
```python
def multiply_by_two(x):

    return x * 2
help(multiply_by_two)
```
**Ejercicio 3
```python
def apply_func_twice (func,arg):

    return func(func(arg))

  

def add_five(x):

    return x + 5

  

print(apply_func_twice(add_five,160))
```
## Uso de listas 
**Ejercicio 4
Destino según tu signo
```python
def obtener_destino(signo):

    signos_zodiaco = ["aries", "tauro", "geminis", "cancer", "leo", "virgo", "libra", "escorpio", "sagitario", "capricornio", "acuario", "piscis"]

    destinos = [

        ["Un día lleno de energía y desafíos emocionantes te espera. ¡Aprovecha al máximo!", "Color de la suerte: Rojo"],

        ["Hoy es un buen día para cuidar de ti mismo/a. Dedica tiempo a tus pasiones y aficiones.", "Color de la suerte: Verde"],

        ["La comunicación será clave hoy. Mantén conversaciones abiertas y honestas.", "Color de la suerte: Amarillo"],

        ["Confía en tu intuición hoy. Te guiará hacia decisiones sabias y acertadas.", "Color de la suerte: Plateado"],

        ["Tu carisma estará en su punto más alto hoy. Aprovecha para destacar en lo que haces.", "Color de la suerte: Dorado"],

        ["Es un buen momento para organizar y planificar tus objetivos a corto plazo.", "Color de la suerte: Azul"],

        ["Hoy será un día equilibrado y armonioso. Busca la belleza en todo lo que te rodea.", "Color de la suerte: Rosa"],

        ["Emociones intensas te aguardan hoy. Aprovecha para profundizar en tus sentimientos.", "Color de la suerte: Morado"],

        ["Explora nuevas ideas y aventuras hoy. La curiosidad te llevará lejos.", "Color de la suerte: Naranja"],

        ["Es un buen momento para enfocarte en tus metas a largo plazo. Ve paso a paso.", "Color de la suerte: Marrón"],

        ["Hoy será un día de libertad y originalidad. Sigue siendo auténtico/a.", "Color de la suerte: Turquesa"],

        ["Escucha tu intuición y tu corazón hoy. Puede haber conexiones emocionales significativas.", "Color de la suerte: Violeta"]

    ]

  

    signo_lower = signo.lower()

    if signo_lower in signos_zodiaco:

        index = signos_zodiaco.index(signo_lower)

        return destinos[index]

    else:

        return ["Lo siento, no se encontró información para ese signo. Introduce un signo válido."]

  

# Solicitar el signo del zodiaco al usuario

signo_zodiaco = input("Introduce tu signo del zodiaco: ")

  

# Obtener el destino para el signo ingresado

resultado = obtener_destino(signo_zodiaco)

  

# Imprimir el resultado

for mensaje in resultado:

    print(mensaje)
```

**Ejercicio 5
```python
s = "Hello, M,a,r,s"

print(s.split(","))
```
**Ejercicio 6
```python
planets=[

    'Mercury','Venus','Earth',

    'Mars','Jupiter','Saturn',

    'UranUs','Neptune'

]

planet_initials={

    planet: planet[0]

    for planet in  planets

}

print(planet_initials)
```


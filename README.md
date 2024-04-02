# Reto_7

### 1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

```
i = 1
while i <= 100:
    print(f"Número: {i}, Cuadrado: {i**2}")
    i += 1
```

```mermaid
flowchart TD
A(Inicio)-->B[i=1]
B-->C{i<=100}
C-->|V|D[Numero: i. Cuadrado: i**2]
D-->F[i=i+1]
F-->C
C-->|F|E(Fin)
```

### 2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.

```
print("Números impares:")
i = 1
while i <= 999:
    print(i)
    i += 2


print("\nNúmeros pares:")
i = 2
while i <= 1000:
    print(i)
    i += 2
```

```mermaid
flowchart TD
A(Inicio)-->B[i=1]
B-->C{i<999}
C-->|V|D[i]
D-->E[i=i+2]
E-->C
C-->|F|F(Fin)

a(Inicio)-->b[i=2]
b-->c{i=1000}
c-->|V|d[i]
d-->e[i=i+2]
e-->c 
c-->|F|f(Fin)
```

### 3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado

```
n = int(input("Ingrese un número natural mayor o igual a 2: "))

if n >= 2:
    print("\nNúmeros pares descendentes hasta 2:")
    i = n if n % 2 == 0 else n - 1  
    while i >= 2:
        print(i)
        i -= 2
else:
    print("El número ingresado no es válido.")
```

```mermaid
flowchart TD
A(Inicio)-->B[Ingresar numero n]
B-->C{n>=2}
C-->|si|D{¿n%2==0?}
D-->|si|E[n=i]
D-->|no|F[i=n-1]
E-->G{i>=2}
F-->G
G-->|V|H[i]
H-->I[i=i-2]
G-->|F|J(Fin)
C-->|no|J
I-->G
```

### 4. En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18.9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.

```
poblacion_a = 25
poblacion_b = 18.9
tasa_crecimiento_a = 0.02
tasa_crecimiento_b = 0.03
anio = 0

while poblacion_b <= poblacion_a:
    poblacion_a *= (1 + tasa_crecimiento_a)
    poblacion_b *= (1 + tasa_crecimiento_b)
    anio += 1

print(f"En el año {2022 + anio} la población del país B ({poblacion_b:.2f} millones) superará a la del país A ({poblacion_a:.2f} millones).")
```

### 5. Imprimir el factorial de un número natural n dado.

```
n = int(input("Ingrese un número natural para calcular su factorial: "))
factorial = 1

if n >= 0:
    i = 1
    while i <= n:
        factorial *= i
        i += 1

    print(f"El factorial de {n} es {factorial}")
else:
    print("El número ingresado no es válido.")
```

### 6. Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.

```
print("Piensa en un número del 1 al 100 y yo trataré de adivinarlo.")
inferior = 1
superior = 100
respuesta = ""

while respuesta != "igual":
    intento = (inferior + superior) // 2
    respuesta = input(f"¿Es {intento} mayor, menor o igual al número que pensaste? ").lower()

    if respuesta == "mayor":
        inferior = intento + 1
    elif respuesta == "menor":
        superior = intento - 1
    elif respuesta != "igual":
        print("Por favor, ingresa 'mayor', 'menor' o 'igual'.")

print(f"¡Adiviné! Tu número es {intento}.")
```

### 7. Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.

```
numero = int(input("Ingrese un número entre 2 y 50: "))

if 2 <= numero <= 50:
    print(f"Los divisores de {numero} son:")
    divisor = 1
    while divisor <= numero:
        if numero % divisor == 0:
            print(divisor)
        divisor += 1
else:
    print("El número ingresado no está dentro del rango válido.")
```

### 8. Implementar el algoritmo que muestre los números primos del 1 al 100. Nota: use funciones

```
print("Números primos del 1 al 100:")
num = 2

while num <= 100:
    divisor = 2
    primo = True

    while divisor < num:
        if num % divisor == 0:
            primo = False
            break
        divisor += 1

    if primo:
        print(num)

    num += 1
```

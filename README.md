# Reto_7

### 1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.

```
i = 1
while i <= 100:
    print(f"Número: {i}, Cuadrado: {i**2}")
    i += 1
```

```flowchart TD
A(Inicio)-->B[i=1]
B-->C{i<=100}
C-->|si|D[Numero: i. Cuadrado: i**2]
D-->C
C-->|no|E(Fin)
```

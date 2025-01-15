# R7-For-ever
**Nota:** en lo posible se escribora la posible salida del programa si no es muy extenza, en caso de que no este se le anima a probarlos en un interprete, disculpe las molestias
## Retos
1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
#### Programa
```python
for num in range(1, 101): #Rango de 1 hasta 100
  print("Número:",num ,"Cuadrado:",num**2)
```   
2. Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
#### Programa
```python
#El incremento sera de 2 en 2 como indica el 3er numero de ambos rangos
print("Números impares:")
for imp in range(1, 1000, 2): #desde 1 hasta 999
  print(imp)
print("\nNúmeros pares:") #El \n es unicamente para fines "esteticos"
for par in range(2, 1001, 2): #desde 2 hasta 1000
  print(par)
```  
3. Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
#### Programa
```python
n=int(input("Ingresa un numero mayor o igual a 2: "))
if n >= 2: #Si la condicion se cumple se ejecutara el programa
  #Comprobador de pares:
  if n%2 == 0:
    n_def = n  #Si n es par, comenzamos desde n
  else:
    n_def = n - 1  #Si n es impar, comenzamos desde n-1 (el mayor par menor que n)       
  for n_par in range(n_def, 2, -2):  # Rango de números pares, reduciendo de 2 en 2 desde el n_definido
    print(n_par)
else:
  print("El número debe ser mayor o igual a 2")
```
4. Imprimir los números de 1 hasta un número natural n dado, cada uno con su respectivo factorial
#### Programa
```python
n=int(input("Ingresa un numero mayor o igual a 1: "))
if n >= 1: #Condicion inicial
    # Imprimir cada número de 1 a n con su respectivo factorial
    for i in range(1, n + 1): # +1 para que entre en el rango el n anterior
        # Calcular el factorial: Leer nota abajo
        acumulado = 1
        for f in range(1, i + 1):
            acumulado *= f  # Multiplicamos los números consecutivos
        print("Número:", i,"Factorial:",acumulado) 
else:
    print("El número debe ser mayor o igual a 1.")
```
**Nota:** Se tomo inspiracion de: https://github.com/Felip-UN/Bucles-R6?tab=readme-ov-file#4-imprimir-el-factorial-de-un-n%C3%BAmero-natural-n-dado ya que hablaba de un mismo tema
5. Calcular el valor de 2 elevado a la potencia n usando ciclos for.
#### Programa
```python
n = int(input("Introduce un número mayor o igual a 0: "))
potencia = 1 # Inicializamos el resultado en 1, ya que cualquier número elevado a la potencia 0 es 1
for i in range(n):
    potencia*= 2  # Multiplicamos el resultado por 2 en cada iteración/repeticion
    #El valor se actualizara con cada repeticion y solo se imprimira:
print("2 elevado a ", n,"es:",potencia) #El deseado
```
Version variada para ver todos los pasos, este imprimira lo que se describio en la linea 5
```python
n = int(input("Introduce un número mayor o igual a 0: "))
potencia = 1 # Inicializamos el resultado en 1, ya que cualquier número elevado a la potencia 0 es 1
for i in range(n):
    potencia*= 2  # Multiplicamos el resultado por 2 en cada iteración/repeticion
    print(potencia)
print("2 elevado a ", n,"es:",potencia)
```
6. Leer un número natural n, leer otro dato de tipo real x y calcular x^n usando ciclos for. Disclaimer: Trate de no utilizar el operador de potencia (**)
#### Programa
```python
n = int(input("Introduce un número natural >= 0: "))
x = float(input("Introduce un número real: "))
potencia = 1 #Inicializamos el resultado en 1, ya que cualquier número elevado a la potencia 0 es 1
for i in range(n): #se ejecuta n veces, en cada iteración multiplicamos el valor actual de resultado por x.
    potencia *= x  #Multiplicamos el resultado por x en cada iteración
print(x,"elevado a ",n ,"es:", potencia) #Solo imprimimos el resultado deseado, que sera el ultimo del bucle
```
7. Diseñe un programa que muestre las tablas de multiplicar del 1 al 9.
#### Programa
```python
for tabla in range(1, 10):  #Bucle para las tablas del 1 al 9
  print("\nTabla de multiplicar del", tabla) 
  #Bucle para mostrar las multiplicaciones de la tabla actual:
  for n1_10 in range(1, 11):  #Ciclo para multiplicar de 1 a 10
    salida = tabla * n1_10
    print(tabla,"x", n1_10,"=",salida)
```
8. Diseñar una función que permita calcular una aproximación de la función exponencial alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. **Nota:** use *math* para traer la función exponencial y mostrar la diferencia entre el valor real y la aproximación.
$$e^x \approx exp(x,n) \approx \sum_{i=0}^{n}\frac{x^i}{i!}$$
9. Diseñar una función que permita calcular una aproximación de la función seno alrededor de 0 para cualquier valor x (real), utilizando los primeros n términos de la serie de Maclaurin. **Nota:** use *math* para traer la función seno y mostrar la diferencia entre el valor real y la aproximación.
$$sin(x) \approx sin(x,n) \approx \sum_{i=0}^{n} (-1)^i \frac{x^{2i+1}}{(2i+1)!}$$

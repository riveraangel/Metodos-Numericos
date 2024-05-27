# Descripción

El método de Simpson 1/3 es otro método de integración numérica que aproxima el valor de una integral definida utilizando polinomios de segundo grado (parábolas) para aproximar la función integrada.
Para el ejercicio planteado en la regla de trapecio, usando cuatro tramos, se aplica el método cada dos tramos.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4bb75fb4-9d91-480e-9b45-cb3b5d80e30d)

Tramos = 4

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/506b13b2-29f8-4b6e-ac77-9e90dfecdf2e)

Note que al usar Simpson 1/3 con 4 tramos el resultado tiene los 2 primeros decimales iguales a usar Trapecio con 16 tramos.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5c35fd97-8dcd-4881-838b-601208ed8586)


# Algoritmo


Es el resultado cuando se realiza una interpolación con polinomio de segundo grado.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/47bd0847-0adf-42e4-85e6-9f912a2bbed3)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/15428604-943a-4001-a08f-4297e281602c)

Usando un polinomio de Lagrange de segundo grado:

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5564596d-362a-4ab0-a245-4951e0a0ae2a)

Que tiene como resultado para un solo tramo:

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2fd661b7-2142-47ea-bced-6effa7bec6c4)


Siendo:

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/bad4d30e-dec4-4f98-a8fb-d8716f3aafd3)


# Implementación en Java
    
       import sympy as sp
    
    # Definir la variable simbólica
    x = sp.symbols('x')
    
    # Entrada de la función como texto
    f_input = input('f(x)= ')
    # Convertir la entrada de texto a una expresión de Sympy
    g = sp.lambdify(x, sp.sympify(f_input), 'numpy')
    
    # Entrada de los límites de integración
    a = float(input('Limite inferior: '))
    b = float(input('Limite superior: '))
    
    # Cálculo del intervalo h
    h = (b - a) / 3
    
    # Cálculo de la integral usando la regla de Simpson 3/8
    I = (3 * h / 8) * (g(a) + 3 * g((2 * a + b) / 3) + 3 * g((a + 2 * b) / 3) + g(b))
    
    # Mostrar el resultado
    print('Valor Aproximado de la Integral:', I)


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/5f5c2ad6-5330-4ba4-96c0-27edbc5b8048)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/8eed2f17-963a-4830-9e8c-080db9bf7f35)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/23add6a4-da66-4b9d-8637-c763dce99d3a)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/58add6ca-08af-4127-9de3-36354c127485)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/33e27776-93d0-4201-bb68-bdc6decf6b7b)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4e2ab001-f92e-423f-8a4c-1b671545f656)


# Ejercicio 3

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/b1add599-0ccf-40f5-a883-335b661f4a4e)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/bf107a6d-d8ee-44f3-a390-34e37fa3785f)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9803d955-1259-42f9-9799-26e1b3afc6a0)


# Ejercicio 4

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/bd54619c-16dc-4971-8843-9da59f9360c5)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/da18a0ba-af78-4b31-a572-4ac1e3e77149)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/42139019-9d61-401f-9b99-f3158ce7c9c7)


# Descripción

Es el resultado cuando para el integral se utiliza el resultado de una interpolación con polinomio de tercer grado.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e00f3155-87d5-4ae7-9b30-819d2aa668a8)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/76e42ca3-593d-4661-90da-e1d1e90041a9)

Al desarrollar la fórmula se la fórmula de la Regla de Simpson de 3/8 para un segmento con tres tramos con distancia h:

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/0878f29b-b1c3-4994-b3ab-597497296723)

Siendo el tramo de un segmento [a,b]

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/00c4cd07-f310-44bf-a1a7-67b182f1e44f)


# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c35b5282-b39e-4624-a6f9-256af159231a)


# Implementación en Python

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

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/ef1f672e-bfcc-4c7d-9bb2-f495ace23c05)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4ba5ebca-6f29-4e8e-8356-de65bf31fc6d)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a3d2251b-c107-4b63-be44-61722ecb1478)



# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9a6d36aa-9fcb-4d88-98d4-5578752acef4)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/990e5cc0-40e8-41a9-b8ed-8f90a35e1e3f)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/8894f113-96cd-4457-b0fb-cb9cd78d4f22)

# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/cb0ee75f-b328-4db3-a2ea-6a64869d82d3)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c66e7b40-d45e-464b-b637-67baf85a21f2)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e618afe7-acd3-453d-99b2-a89221489e8a)

# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e02703e1-26bd-460e-aa33-0d8074e070d3)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/323b141f-e4b3-4daa-8a5b-6c5c6f5917b5)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/b56f38c5-5803-4da6-a871-dad57b9accf7)


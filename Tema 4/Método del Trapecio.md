
# Descripción

La regla del trapecio es uno de los métodos más utilizados para calcular aproximaciones numéricas de integrales definidas. Es la primera de las fórmulas cerradas de integración de  Newton – Cotes.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/065089d3-592a-4323-8a0c-0fb200982231)

El método del trapecio es una técnica de integración numérica que aproxima la integral definida de una función 
𝑓 (𝑥) en el intervalo [𝑎,𝑏] mediante la suma de áreas de trapecios. La fórmula básica del método del trapecio 
se puede derivar al aproximar la función por una línea recta entre dos puntos consecutivos y calcular el área bajo esta línea.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7bf549bb-5a95-41bf-b910-f0b038f57741)

# Implementación en Python

    import numpy as np
    import matplotlib.pyplot as plt
    
    fx = lambda x: np.sqrt(x)*np.sin(x)
    
    a = 1
    b = 3
    tramos = 4
    
    h = (b-a)/tramos
    xi = a
    suma = fx(xi)
    for i in range(0,tramos-1,1):
        xi = xi + h
        suma = suma + 2*fx(xi)
    suma = suma + fx(b)
    area = h*(suma/2)
    
    # Redondear la variable area a tres decimales
    
    
    print ('Tramos: ', tramos)
    print ('Integral: ', area)
    
    area = round(area, 3)
    print ('Integral limitada: ', area)


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4bbef26c-3da0-4c6d-827b-73d7338d231b)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a5796585-d85d-45c6-a13d-ed1a3caac2f9)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7b074111-c1c0-40d4-b33f-a5f970f73c26)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d627dc4f-b863-4584-9cc1-26711a33b850)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3d4dd77d-100a-4ebc-86b3-52d30fbb487e)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/721ab5dc-4038-440e-a7cc-b4d58d9f2285)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/db4446b3-a68b-46f0-9ac8-df1a6d252bd9)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3f67b085-7e58-48f7-90c1-ecc5aecb24a9)


### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6ef08345-c689-4e53-baf2-0099df7479f6)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/33222f06-5024-459d-a267-169a269dc5fb)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e90c1108-7338-44fe-8e94-f3bd2e05474c)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6b8b5e69-bd45-4d45-8d1b-cec78efc6725)

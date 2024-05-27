# Descripción


El método de Simpson 1/3 es otro método de integración numérica que aproxima el valor de una integral definida utilizando polinomios de segundo grado (parábolas) para aproximar la función integrada. 

Para el ejercicio planteado en la regla de trapecio, usando cuatro tramos, se aplica el método cada dos tramos.

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/d288ccc3-fe41-428f-b968-8f734290dabd)

Tramos = 4

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/b6016f62-7b72-452f-aaeb-41251658d641)

Note que al usar Simpson 1/3 con 4 tramos el resultado tiene los 2 primeros decimales iguales a usar Trapecio con 16 tramos.

Resultado:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/439fbe0e-4efd-42de-a61e-e97e17cdd733)

# Algoritmo


Es el resultado cuando se realiza una interpolación con polinomio de segundo grado.

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/cff5cb50-4e05-42e5-b2ab-b96bb43734d3)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/e50a81a3-6162-4855-9ac3-2e90859f6e13)

Usando un polinomio de Lagrange de segundo grado:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/7ec24145-68be-47f3-9e2e-c1a9b9ba3ec4)

Que tiene como resultado para un solo tramo:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/27364eba-5879-49b4-a5a7-594a979d32f6)

Siendo:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/c8410d6f-3d28-4fa2-a2cf-1f1e7c9c6100)



# Implementación en Java
    



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


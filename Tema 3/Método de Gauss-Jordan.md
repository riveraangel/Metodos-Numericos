# Descripción

El método de eliminación Gauss-Jordan consiste en representar el sistema de ecuaciones por medio de una matriz y obtener a partir de ella lo que se define como la matriz escalonada equivalente, a través de la cual se determina el tipo de solución de la ecuación.

Un tipo de matriz escalonada (también conocida como matriz de identidad, donde la diagonal principal tiene solamente uno y, en el resto de las posiciones, cero) se representa de la siguiente forma:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/bafc2a1a-26ea-4468-bdfb-faa998d619f0)

# Algoritmo

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/019b9e41-db20-4c04-a181-3b9497f4fcf6)


![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/fb228c5a-04a7-4b06-a002-310034230569)


![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/f0c24a02-20e9-43d7-85d4-7a747939fff0)

# Implementación en Java

    public class GaussJordan {
    
        public static void main(String[] args) {
            double[][] matriz = {
                {4, 2, 5, 60.70},
                {2, 5, 8, 92.90},
                {5, 4, 3, 56.30}
            };
    
            gaussJordan(matriz);
    
            imprimirSolucion(matriz);
        }
    
        public static void gaussJordan(double[][] matriz) {
            int filas = matriz.length;
            int columnas = matriz[0].length;
    
            for (int i = 0; i < filas; i++) {
                double divisor = matriz[i][i];
                for (int j = 0; j < columnas; j++) {
                    matriz[i][j] /= divisor;
                }
    
                for (int k = 0; k < filas; k++) {
                    if (k != i) {
                        double factor = matriz[k][i];
                        for (int j = 0; j < columnas; j++) {
                            matriz[k][j] -= factor * matriz[i][j];
                        }
                    }
                }
            }
        }
    
        public static void imprimirSolucion(double[][] matriz) {
            int filas = matriz.length;
            int columnas = matriz[0].length;
            for (int i = 0; i < filas; i++) {
                System.out.print("x" + (i + 1) + " = ");
                System.out.printf("%.2f%n", matriz[i][columnas - 1]);
            }
        }
    }


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3a86db31-1454-4bd1-bee2-75cb9df0d75a)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/81155286-ac6d-40a2-94a8-b9314745b48a)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/668c26d1-f02f-43ae-8c76-1ea653797da5)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4e167aa5-b174-4b0b-9ca6-63bc4de23d7d)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2d7895e7-ccbd-4e32-ac86-66b9f88efba3)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/bc4c1153-3bc2-45f7-98d0-1bfb62141391)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/04cf3653-7a2e-4611-bb08-1fca74312d56)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7c7fbd57-af46-4eae-88fa-6dce6422a339)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/0e049e41-e22c-4f6a-8033-dffc05e70e1a)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6178a00a-ea3c-4500-9ae5-09e0f18d3c47)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2a0dbf73-ca45-4845-958b-c8930887384e)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9d886218-bb73-4716-9644-d66160540bb0)




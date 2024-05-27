# Descripción

El método de eliminación Gaussiana es una técnica fundamental en el ámbito del álgebra lineal, utilizado para resolver sistemas de ecuaciones lineales. 
Este método, también conocido como eliminación de Gauss, busca transformar un sistema de ecuaciones lineales en uno equivalente más simple, lo que permite encontrar fácilmente las soluciones.

# Algoritmo

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/1f8ea584-6fb3-41f6-9334-cb8191ee8a57)

Pasos principales:

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/aa413f14-a8c5-4c4e-a066-141d01cc0062)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/c09efb2f-f838-47c1-8124-c91481575bc0)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/fa16db06-f336-49bc-b24e-5b1288cb7bd3)


![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/f679851b-28a6-408d-b0c0-528dcb926574)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/fb03c1f4-8f49-4ed4-aeab-9603fae037da)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/ab33716b-e87d-4645-81b3-78e58981de03)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/2f1672fd-b993-4d23-b763-2e0b3609a82b)


# Implementación en Java

        public class EliminacionGaussiana {
        
        public static void eliminacionGaussiana(double[][] matriz) {
            int filas = matriz.length;
            int columnas = matriz[0].length;
            
            for (int k = 0; k < filas - 1; k++) {
                for (int i = k + 1; i < filas; i++) {
                    double factor = matriz[i][k] / matriz[k][k];
                    for (int j = k; j < columnas; j++) {
                        matriz[i][j] -= factor * matriz[k][j];
                    }
                }
            }
        }
    
        public static void main(String[] args) {
            double[][] matriz = {
                {2, 1, -1, 8},
                {-3, -1, 2, -11},
                {-2, 1, 2, -3}
            };
    
            eliminacionGaussiana(matriz);
    
            // Imprimir la matriz después de la eliminación gaussiana
            System.out.println("Matriz despues de la eliminacion gaussiana:");
            for (int i = 0; i < matriz.length; i++) {
                for (int j = 0; j < matriz[0].length; j++) {
                    System.out.printf("%.2f\t", matriz[i][j]);
                }
                System.out.println();
            }
        }
    }


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema



### Solución analítica



### Solución con código




# Ejercicio 2

### Problema




### Solución analítica




### Solución con código




# Ejercicio 3

### Problema



### Solución analítica



### Solución con código




# Ejercicio 4

### Problema



### Solución analítica



### Solución con código



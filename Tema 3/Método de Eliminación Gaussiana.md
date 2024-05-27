# Descripción

El método de Gauss opera sobre la matriz aumentada y pivoteada por filas, añadiendo el proceso de «eliminación hacia adelante» mediante la operación entre filas. 

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

                import java.util.Arrays;
        
        public class MetodoGauss {
        
            public static void main(String[] args) {
                double[][] A = {
                    {4, 2, 5},
                    {2, 5, 8},
                    {5, 4, 3}
                };
        
                double[][] B = {
                    {60.70},
                    {92.90},
                    {56.30}
                };
        
                double casicero = 1e-15; // Considerar como 0
        
                double[][] AB = new double[A.length][A[0].length + 1];
                for (int i = 0; i < A.length; i++) {
                    for (int j = 0; j < A[i].length; j++) {
                        AB[i][j] = A[i][j];
                    }
                    AB[i][A[i].length] = B[i][0];
                }
        
                double[][] AB0 = new double[AB.length][AB[0].length];
                for (int i = 0; i < AB.length; i++) {
                    AB0[i] = Arrays.copyOf(AB[i], AB[i].length);
                }
        
                int n = AB.length;
                int m = AB[0].length;
        
                for (int i = 0; i < n - 1; i++) {
                    // columna desde diagonal i en adelante
                    double[] columna = new double[n - i];
                    for (int k = i; k < n; k++) {
                        columna[k - i] = Math.abs(AB[k][i]);
                    }
                    int dondemax = i + encontrarMaximoIndice(columna);
        
                    if (dondemax != 0) {
                        // intercambia filas
                        double[] temporal = Arrays.copyOf(AB[i], AB[i].length);
                        AB[i] = Arrays.copyOf(AB[dondemax], AB[dondemax].length);
                        AB[dondemax] = Arrays.copyOf(temporal, temporal.length);
                    }
                }
        
                double[][] AB1 = new double[AB.length][AB[0].length];
                for (int i = 0; i < AB.length; i++) {
                    AB1[i] = Arrays.copyOf(AB[i], AB[i].length);
                }
        
                for (int i = 0; i < n - 1; i++) {
                    double pivote = AB[i][i];
                    for (int k = i + 1; k < n; k++) {
                        double factor = AB[k][i] / pivote;
                        for (int j = i; j < m; j++) {
                            AB[k][j] -= AB[i][j] * factor;
                        }
                    }
                }
        
                int ultfila = n - 1;
                int ultcolumna = m - 1;
                double[] X = new double[n];
        
                for (int i = ultfila; i >= 0; i--) {
                    double suma = 0;
                    for (int j = i + 1; j < ultcolumna; j++) {
                        suma += AB[i][j] * X[j];
                    }
                    double b = AB[i][ultcolumna];
                    X[i] = (b - suma) / AB[i][i];
                }
        
                System.out.println("Matriz aumentada:");
                imprimirMatriz(AB0);
                System.out.println("Pivoteo parcial por filas:");
                imprimirMatriz(AB1);
                System.out.println("Eliminacion hacia adelante:");
                imprimirMatriz(AB);
                System.out.println("Solucion:");
                imprimirVector(X);
            }
        
            public static int encontrarMaximoIndice(double[] arreglo) {
                int indiceMaximo = 0;
                for (int i = 1; i < arreglo.length; i++) {
                    if (arreglo[i] > arreglo[indiceMaximo]) {
                        indiceMaximo = i;
                    }
                }
                return indiceMaximo;
            }
        
            public static void imprimirMatriz(double[][] matriz) {
                for (double[] fila : matriz) {
                    for (double elemento : fila) {
                        System.out.printf("%.2f\t", elemento);
                    }
                    System.out.println();
                }
            }
        
            public static void imprimirVector(double[] vector) {
                for (double elemento : vector) {
                    System.out.printf("%.2f\t", elemento);
                }
                System.out.println();
            }
        }



El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3a86db31-1454-4bd1-bee2-75cb9df0d75a)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/81155286-ac6d-40a2-94a8-b9314745b48a)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d8eb5451-4005-453a-8a37-27fd2cb87850)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4e167aa5-b174-4b0b-9ca6-63bc4de23d7d)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2d7895e7-ccbd-4e32-ac86-66b9f88efba3)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/599c52d0-f0ff-4c2f-9be8-1b7c31ebc22f)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/04cf3653-7a2e-4611-bb08-1fca74312d56)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7c7fbd57-af46-4eae-88fa-6dce6422a339)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/206333ed-5360-4a51-a607-36703821ea54)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6178a00a-ea3c-4500-9ae5-09e0f18d3c47)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2a0dbf73-ca45-4845-958b-c8930887384e)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6c36a77d-40b1-4f86-a58b-16f17cb7d35b)


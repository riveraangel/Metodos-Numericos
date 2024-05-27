# Descripción

El método de Gauss-Seidel es un algoritmo iterativo utilizado para resolver sistemas de ecuaciones lineales. Es una extensión del método de Jacobi y se utiliza principalmente para resolver sistemas de ecuaciones lineales grandes y dispersos.

El método de Gauss-Seidel es un método iterativo utilizado para resolver sistemas de ecuaciones lineales 
𝐴 𝑥 = 𝑏, donde  𝐴 es una matriz cuadrada de coeficientes,  𝑥 es el vector de incógnitas y  𝑏 es el vector de términos constantes.

# Algoritmo

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/052616c3-d150-48fb-aa29-d3e6e9ab6232)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/8e3dfff3-47ca-4b41-ac5a-fd8bf00c523e)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/acfac799-23c9-4e59-b402-25ca87dfb531)


# Implementación en Java

    import java.util.Arrays;
        import java.util.Scanner;
    
    public class Gauss_Seidel {
  
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese el número de ecuaciones: ");
        int n = scanner.nextInt();

        double[][] coeficientes = new double[n][n];
        double[] b = new double[n];

        System.out.println("Ingrese los coeficientes de las ecuaciones:");
        for (int i = 0; i < n; i++) {
            System.out.printf("Ecuación %d:\n", i + 1);
            for (int j = 0; j < n; j++) {
                System.out.printf("Coeficiente %d: ", j + 1);
                coeficientes[i][j] = scanner.nextDouble();
            }
            System.out.print("Término independiente: ");
            b[i] = scanner.nextDouble();
        }

        System.out.print("Ingrese el porcentaje de error aceptado: ");
        double error = scanner.nextDouble();

        double[] resultados = gaussSeidel(coeficientes, b, error);

        System.out.println("Resultados:");
        for (int i = 0; i < n; i++) {
            System.out.printf("x%d = %.4f\n", i + 1, resultados[i]);
        }

        scanner.close();
    }

    public static double[] gaussSeidel(double[][] coeficientes, double[] b, double error) {
        int n = b.length;
        double[] resultados = new double[n];
        double[] nuevosResultados = new double[n];
        double[] errores = new double[n];
        double maxError;

        for (int i = 0; i < n; i++) {
            resultados[i] = 0; // Suponer todos los resultados iniciales como 0
        }

        do {
            // Calcular los nuevos resultados
            for (int i = 0; i < n; i++) {
                double sum = 0;
                for (int j = 0; j < n; j++) {
                    if (j != i) {
                        sum += coeficientes[i][j] * resultados[j];
                    }
                }
                nuevosResultados[i] = (b[i] - sum) / coeficientes[i][i];
            }

            maxError = 0;
            for (int i = 0; i < n; i++) {
                errores[i] = Math.abs((nuevosResultados[i] - resultados[i]) / nuevosResultados[i]);
                if (errores[i] > maxError) {
                    maxError = errores[i];
                }
            }

            System.arraycopy(nuevosResultados, 0, resultados, 0, n);

        } while (maxError > error);

        return resultados;
    }
    }



El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/4cbd4f9e-ea75-46a0-b856-2d782a2f03b9)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/57d7815d-9a87-47c4-b6ee-e4c6c28ecf6c)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/c3b02a10-6941-4c22-903f-c3f4feb64d66)


# Ejercicio 2

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/d259828d-71dc-4fa6-979d-7a369f725f8d)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/cb69809f-b11e-4ef0-8f7a-a65334711bce)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/9f3b8eca-1a31-4d19-a05b-b87cfc8eecb6)


# Ejercicio 3

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/3b0a1a49-be6f-45f3-8f42-5a10d1ad0f60)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/d17a1ab8-5e0f-4388-a44d-b99ff59f8d7d)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/9e4de426-a38c-4c4e-a964-75be11fc3666)


# Ejercicio 4

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/5e7c688b-de43-4554-a4bf-b1272722a61c)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/a52a125b-b3a7-44bd-86f8-16b3c6b3eee2)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/ea410bbf-3e96-44e1-873d-8fa0ae765f1d)



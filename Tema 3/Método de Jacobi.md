# Descripción

Los métodos iterativos de Jacobi y Gauss-Seidel son los procesos de aproximaciones sucesivas
para resolver sistemas de ecuaciones lineales compatibles determinados. Ambos requieren de la
verificación de un criterio de convergencia comúnmente conocido como diagonal pesada. Son
alternativas interesantes para ser programadas por su relativa simplicidad.

# Algoritmo

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/2067266e-6a27-4679-8a92-c6f77d112906)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/76d07da4-83ac-4c70-ab72-6e297c50b5c4)

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/2abd81ab-72e7-4ae4-ae41-4d9d91654e40)


# Implementación en Java
    
    import java.util.Scanner;
    
    public class MetodoJacobi {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
    
        // Solicitar el tamaño del sistema
        System.out.print("Ingrese el tamaño del sistema: ");
        int tam = sc.nextInt();
    
        // Validar el tamaño del sistema
        if (tam < 2) {
            System.out.println("El tamaño del sistema debe ser mayor o igual a 2.");
            return;
        }
    
        // Solicitar la matriz de coeficientes y el vector de resultados
        double[][] matrizCoeficientes = new double[tam][tam];
        double[] vectorResultados = new double[tam];
    
        System.out.println("Ingrese la matriz de coeficientes:");
        for (int i = 0; i < tam; i++) {
            for (int j = 0; j < tam; j++) {
                System.out.print("Ingrese el elemento [" + (i + 1) + "][" + (j + 1) + "]: ");
                matrizCoeficientes[i][j] = sc.nextDouble();
            }
        }
    
        System.out.println("Ingrese el vector de resultados:");
        for (int i = 0; i < tam; i++) {
            System.out.print("Ingrese el elemento [" + (i + 1) + "]: ");
            vectorResultados[i] = sc.nextDouble();
        }
    
        // Definir el vector inicial (se quedan en 0)
        double[] vectorInicial = new double[tam];
        double[] vectorAnterior = new double[tam];
    
        int maxIteraciones = 50;
    
        // Realizar iteraciones en el método de Jacobi
        for (int k = 0; k < maxIteraciones; k++) {
            System.out.print("Iteración " + (k + 1) + ": ");
    
            // Calcular nuevos valores de x
            double[] x = new double[tam];
            for (int i = 0; i < tam; i++) {
                double sum = 0;
                for (int j = 0; j < tam; j++) {
                    if (j != i) {
                        sum += matrizCoeficientes[i][j] * vectorInicial[j];
                    }
                }
                x[i] = (vectorResultados[i] - sum) / matrizCoeficientes[i][i];
            }
    
            double errorAbsoluto = calcularErrorAbsoluto(x, vectorAnterior);
    
            if (k > 0 && errorAbsoluto < 0.05) {
                System.out.println("Error absoluto menor al 5% en la iteración " + (k + 1) + ".");
                break; // Romper el ciclo
            }
    
            // Mostrar resultados de la iteración
            for (int i = 0; i < tam; i++) {
                System.out.printf("x%d = %.4f ", i + 1, x[i]);
            }
            System.out.println();
    
            // Actualizar el vector inicial y el vector anterior para la próxima iteración
            System.arraycopy(x, 0, vectorInicial, 0, tam);
            System.arraycopy(x, 0, vectorAnterior, 0, tam);
        }
    }

private static double calcularErrorAbsoluto(double[] vectorActual, double[] vectorAnterior) {
    double maxError = 0;
    for (int i = 0; i < vectorActual.length; i++) {
        double error = Math.abs((vectorActual[i] - vectorAnterior[i]) / Math.abs(vectorActual[i]));
        maxError = Math.max(maxError, error);
    }
    return maxError;
  }
}



El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/3a7b7c54-71b0-4917-a4ab-87651c38229a)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/80f9aacd-cfb8-4137-9386-446e74138e60)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/378cd176-063e-4faf-88b6-c1969e5132b8)


# Ejercicio 2

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/ee02a67c-2912-41a2-9ed9-d17cc2be8c07)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/e537c406-e1c4-43b6-85e1-29603b4ae907)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/f2cadbc6-2d61-4873-8018-ac6d9fc8419d)

# Ejercicio 3

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/27724aa6-4494-4d1e-a855-9096c08524a5)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/b3fe9e48-d266-4b57-b04a-c2286ede1225)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/6603b8ea-9b88-4a32-80b8-bcef4b0e456d)


# Ejercicio 4

### Problema

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/09309b4d-f0fc-4fd3-84e2-07da29ca7057)

### Solución analítica

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/b6cc311f-24b8-4ece-bb6c-5c394921da5f)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/df439137-f6b1-41d6-820b-b5212b7ca335)

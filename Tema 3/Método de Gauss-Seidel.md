# Descripción

El método de Gauss-Seidel es un algoritmo iterativo utilizado para resolver sistemas de ecuaciones lineales. Es una extensión del método de Jacobi y se utiliza principalmente para resolver sistemas de ecuaciones lineales grandes y dispersos.

El método de Gauss-Seidel es un método iterativo utilizado para resolver sistemas de ecuaciones lineales 
𝐴 𝑥 = 𝑏, donde  𝐴 es una matriz cuadrada de coeficientes,  𝑥 es el vector de incógnitas y  𝑏 es el vector de términos constantes.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d720dbcb-8fa0-4fbb-ba96-9ad3af71e423)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/02cd7984-00cc-4e9e-bbb3-3280774fb524)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d127855c-9c54-474f-8621-f42d646c9b32)


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

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/86d8fa0d-4fe0-446d-9131-db9dfbe2a20a)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/44549b85-5159-4adb-a91a-36b554a30a0a)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d11d2ebe-f4cd-4921-914b-bc25faf31cce)

# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c233c247-b78a-42f2-9ffa-5da3181d6582)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f536d225-28b2-49be-9c85-b609f443a896)

### Solución con código

![image](https://github.com/Jorge11Romero/M-todos-Num-ricos/assets/147437900/9f3b8eca-1a31-4d19-a05b-b87cfc8eecb6)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5e7750ad-8621-4000-a730-6b47a42ba9ae)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d4813f44-9535-4f9e-ad36-e6354294ede3)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7e73d94f-ec38-438d-8c0e-5706e9cf7231)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/edb0fb9c-fbea-4c15-b8e0-25d282fbcc28)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/74eb8a05-f317-4050-bab5-4c49b14da217)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c40fef1b-bf71-43de-98c1-c61d75211da6)




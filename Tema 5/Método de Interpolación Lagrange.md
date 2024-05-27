# Descripción
El polinomio de interpolación de Lagrange es simplemente una reformulación del polinomio
de Newton que evita el cálculo de las diferencias divididas:

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/b77066dd-81da-4a6f-b802-ac1db86608cc)

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/35f21c2e-ffa6-4be8-8466-95032b7f48f8)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/fcd25963-9475-41c6-9b0f-c83e459f63b7)


# Implementación en Java
    
    public class InterpolacionLagrange {
    
        public static double lagrange(double[] x, double[] y, double xi) {
            double resultado = 0.0;
            int n = x.length;
    
            for (int i = 0; i < n; i++) {
                double termino = y[i];
                for (int j = 0; j < n; j++) {
                    if (j != i) {
                        termino *= (xi - x[j]) / (x[i] - x[j]);
                    }
                }
                resultado += termino;
            }
    
            return resultado;
        }
    
        public static void main(String[] args) {
            // Puntos de datos (x, y)
            double[] x = {0, 1, 2, 3};
            double[] y = {1, 3, 2, 5};
    
            double xi = 2.5;
    
            double yi = lagrange(x, y, xi);
            System.out.println("Valor interpolado en x = " + xi + " es y = " + yi);
        }
    }

  
El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5443e172-bed5-42a3-b5a7-984ddcf2582c)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/0c5fb2b6-92d5-48fd-a8fe-a2e201f776b2)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d459b51a-6dbd-4407-87eb-72caaa024ded)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c91517a2-8b88-43ff-8dff-e961d32570bc)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/99a79c38-b335-4d42-8c9c-d92b9c80e08d)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/60937d4b-ff9b-484a-ba0d-07db359baefb)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/fe1cd53c-36ff-42f0-9d64-90fab5b23c77)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2720de2b-90c9-487d-8782-048cf9adf531)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/999f5b99-30c3-43f7-a0ad-a9b2d27df6e3)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/eeeba36f-8725-496e-948f-bd878f101501)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4af850af-bb26-40f2-b247-6ea31dd56e18)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/05c86b01-0bd2-49e0-afd8-9f9cd3fff07d)



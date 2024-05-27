# Descripción

Esta es la forma mas simple de interpolación, consiste en unir
dos puntos con una línea recta. La estrategiaes usar una línea
recta para conectar los datos conocidos a ambos lados del
punto desconocido.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c758785a-7153-4fe9-aae4-27aeaa428906)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e9d8a4c8-65db-425b-8de8-1850aee6642c)


# Algoritmo




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





![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e7b28f1b-f5d1-4487-b922-8093280b59cd)


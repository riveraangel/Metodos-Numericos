# Descripción

Un método en varios pasos o continuo, utiliza los valores de varios pasos calculados con anterioridad para obtener el valor de y n+1 Hay numerosas fórmulas aplicables en la aproximación de soluciones de ecuaciones diferenciales.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/90e71c46-0e90-42bf-ab57-831732923f41)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/921692b1-d600-4569-85a5-1e0833fd5df5)



# Implementación en Java

        import java.util.function.Function;
    
    public class MetodosNumericos {
    
        public static double euler(double x0, double y0, double h, int n, Function<Double, Double> f) {
            double xn = x0;
            double yn = y0;
    
            for (int i = 0; i < n; i++) {
                yn = yn + h * f.apply(xn);
                xn = xn + h;
            }
    
            return yn;
        }
    
        public static double rungeKutta(double x0, double y0, double h, int n, Function<Double, Double> f) {
            double xn = x0;
            double yn = y0;
    
            for (int i = 0; i < n; i++) {
                double k1 = h * f.apply(xn);
                double k2 = h * f.apply(xn + h/2);
                double k3 = h * f.apply(xn + h/2);
                double k4 = h * f.apply(xn + h);
    
                yn = yn + (k1 + 2*k2 + 2*k3 + k4) / 6;
                xn = xn + h;
            }
    
            return yn;
        }
    
        public static void main(String[] args) {
            
            double x0 = 0; 
            double y0 = 1; 
            double h = 0.1; 
            int n = 10; 
    
            Function<Double, Double> f = x -> x + y0; 
    
            double resultadoEuler = euler(x0, y0, h, n, f);
            System.out.println("Resultado utilizando el metodo de Euler: " + resultadoEuler);
    
            double resultadoRK = rungeKutta(x0, y0, h, n, f);
            System.out.println("Resultado utilizando el metodo de Runge-Kutta: " + resultadoRK);
        }
    }

El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5770155d-e245-4b0d-a5e7-9d053ac87d75)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2f864d29-f3a7-4f57-91f5-8c086819d7cb)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e871a0bb-07a7-4228-8182-24118febafaa)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2901274a-21e6-4580-bb89-bd59c25fe403)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c3e21050-d9ce-442c-9f07-367f42c219af)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f87b01ca-20b5-4800-a200-cca9339cfcab)

# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/180dfeb2-1481-489f-a815-1eb3f7b62bc4)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c69d272c-7a12-46a6-913b-4bffc2307d39)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/fba40b91-11a1-4ad1-9163-165a750a137e)

# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/29c48886-48e4-489e-aa4c-68431eb1c7a5)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2b835582-0890-469c-88f6-1c7ea5be1cee)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/560372e1-2d82-41c8-a437-f9641c4e0cb9)


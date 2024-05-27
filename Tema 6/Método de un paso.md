# Descripción

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/bfdc52ba-b8c9-43d3-9cb3-3dc26033cb41)

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/90e71c46-0e90-42bf-ab57-831732923f41)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/921692b1-d600-4569-85a5-1e0833fd5df5)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3a5502f8-6546-401e-894a-ab3725e56143)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3364b3ed-f652-4f7e-a5ba-e9f2f59445c8)

# Implementación en Java
    
    import java.util.function.BiFunction;
    
    public class MetodoUnPaso {
    
        public static double euler(double x0, double y0, double h, int n, BiFunction<Double, Double, Double> f) {
            double xn = x0;
            double yn = y0;
    
            for (int i = 0; i < n; i++) {
                yn = yn + h * f.apply(xn, yn);
                xn = xn + h;
            }
    
            return yn;
        }
    
        public static double rungeKutta(double x0, double y0, double h, int n, BiFunction<Double, Double, Double> f) {
            double xn = x0;
            double yn = y0;
    
            for (int i = 0; i < n; i++) {
                double k1 = h * f.apply(xn, yn);
                double k2 = h * f.apply(xn + h / 2, yn + k1 / 2);
                double k3 = h * f.apply(xn + h / 2, yn + k2 / 2);
                double k4 = h * f.apply(xn + h, yn + k3);
    
                yn = yn + (k1 + 2 * k2 + 2 * k3 + k4) / 6;
                xn = xn + h;
            }
    
            return yn;
        }
    
        public static void main(String[] args) {
            // Valores iniciales
            double x0 = 0;  
            double y0 = 1;  
            double h = 0.1; 
            int n = 10;    
    
            BiFunction<Double, Double, Double> f = (x, y) -> x + y; 
    
    
            double resultadoEuler = euler(x0, y0, h, n, f);
            System.out.println("Resultado utilizando el método de Euler: " + resultadoEuler);
    
            double resultadoRK = rungeKutta(x0, y0, h, n, f);
            System.out.println("Resultado utilizando el método de Runge-Kutta: " + resultadoRK);
        }
    }


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/af6de3d3-ff2f-4191-909f-75c0ddafcce6)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d932ad20-bbd3-4f2a-ab50-67e1ab06d5d4)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6c3cc43e-6995-4079-924d-3d26152e27dd)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/818c6683-466e-4add-80fa-36eea238c5c0)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/82ac493f-034c-44fb-b9fd-2191611314ac)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f90b54e3-2337-40da-ade7-7ad9e054d526)

# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/039486cb-41a2-406e-ac5a-ed570e60ef73)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3318dbc6-ad62-47de-b037-277dceed391e)


### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/25e395f1-f376-4b95-9cc1-78b4138d0448)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e7a04e75-ffb6-4565-a4f0-ffc524aa92ce)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c0cacae6-9a89-4886-ba9b-a759ccad8e93)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/1a677b3f-be0e-4ab4-8148-53e622389b24)

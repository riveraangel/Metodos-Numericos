# Descripción

Los métodos de búsqueda incremental aprovechan la característica localizando
un intervalo en el que la función cambie de signo. Entonces, El método de bisección, también conocido como 
de corte binario, de partición de intervalos o de Bolzano es un algoritmo de búsqueda de raíces que funciona 
dividiendo repetidamente un intervalo en  dos subintervalos y seleccionando el subintervalo en el cual ocurre 
un cambio de signo de la función.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9ba065b6-7a1f-4ca0-b503-942af29f1a07)


# Implementación en Java

    public class Biseccion {
        
        public static double funcion(double x) {
            return x * x - 4;
        }
    
        public static double biseccion(double a, double b, double tolerancia) {
            double c = a;
            while ((b - a) >= tolerancia) {
                c = (a + b) / 2;
                
                if (funcion(c) == 0.0) {
                    break;
                } else if (funcion(c) * funcion(a) < 0) {
                    b = c;
                } else {
                    a = c;
                }
            }
            return c;
        }
    
        public static void main(String[] args) {
            double a = 0, b = 3, tolerancia = 0.0001;
            double raiz = biseccion(a, b, tolerancia);
            System.out.println("La raíz es: " + raiz);
        }
    }

El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/80b13fab-feb0-4e27-97c4-9a70cbaa82a2)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c1a74a0d-6993-45ac-9d81-5ddc144f5d55)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/193ea61d-cff9-4184-890a-721e85ca941c)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/b50954b8-0549-4f46-80fc-611547be35bc)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/821d2615-35ee-473b-9f89-a79779848aa0)


### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7ebf5b3e-9a41-458d-832e-1446ca812f36)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c1efdf09-b482-43ef-bb9c-8b1e4c2c1660)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2f1f1dc4-311a-4db9-b8cd-d60ebae2761c)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/ed0bcd72-644a-4ee3-85a3-92e8221ccf8b)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c7b206a7-244b-4f26-966c-32cac2e4d27f)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f943fdf9-5682-4bd4-a285-600ca9c4960c)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/724ed6cd-59fa-4fef-9ad7-ff8311f9ed85)

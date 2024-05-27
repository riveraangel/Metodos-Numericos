# Descripción

El método de la falsa posición es un algoritmo para encontrar una aproximación de una raíz de una función continua 
𝑓 (𝑥) ) utilizando una combinación de la bisección y la interpolación lineal.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2568315a-bd73-41e2-86b1-7a46cd6330b7)

Representación gráfica delmétodo de la falsa posición.
Con los triángulos semejantes sombreados se obtiene la fórmula para el método.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/684deff0-ce76-47fc-a980-7dbbac5668b0)


# Implementación en Java

        public class FalsaPosicion {
        
        
        public static double funcion(double x) {
            return 4 * x * x - 5 * x;
        }
    
        public static double falsaPosicion(double a, double b, double tolerancia) {
            double c = a;
            while (Math.abs(b - a) >= tolerancia) {
                
                c = a - (funcion(a) * (b - a)) / (funcion(b) - funcion(a));
                
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
            double a = 1, b = 1.6, tolerancia = 0.0001;
            double raiz = falsaPosicion(a, b, tolerancia);
            
            System.out.printf("La raíz es: %.4f%n", raiz);
        }
    }
    

El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/80b13fab-feb0-4e27-97c4-9a70cbaa82a2)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c1a74a0d-6993-45ac-9d81-5ddc144f5d55)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/86634e79-5740-48ad-a4bb-3c7de7546958)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9382a6ce-511b-4a79-bba7-091d99c40eeb)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/6973065c-192e-458a-ac94-24a11466513a)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/cf16eac5-3892-4eff-8bf9-fc3fe9b8efe5)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c1efdf09-b482-43ef-bb9c-8b1e4c2c1660)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2f1f1dc4-311a-4db9-b8cd-d60ebae2761c)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/ed0bcd72-644a-4ee3-85a3-92e8221ccf8b)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2f1ce00b-92bc-4044-bfb6-9add48e991d1)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4d2432ea-cc10-4d7d-b2b9-6399d5474aef)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a0749a10-72ff-46d3-906d-53fa535327a6)


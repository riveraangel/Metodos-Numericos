# Descripción

El método de Newton-Raphson es un algoritmo iterativo para encontrar raíces de una función 
𝑓 (𝑥)  a través de aproximaciones sucesivas basadas en la tangente a la curva de la función en el punto de la aproximación actual.

# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/cac8daf3-7bbe-491a-a67c-814af67a674e)


# Implementación en Java

    public class NewtonRaphson {
        
        public static double funcion(double x) {
            return x * x - 4;
        }
        
        public static double derivada(double x) {
            return 2 * x;
        }
        
        public static double newtonRaphson(double x0, double tolerancia) {
            double x = x0;
            double h = funcion(x) / derivada(x);
            
            while (Math.abs(h) >= tolerancia) {
                h = funcion(x) / derivada(x);
                x = x - h;
            }
            
            return x;
        }
        
        public static void main(String[] args) {
            double x0 = 2; 
            double tolerancia = 0.0001;
            double raiz = newtonRaphson(x0, tolerancia);
            
            System.out.printf("La raíz es: %.4f%n", raiz);
        }
    }
    
El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2342e4d4-6074-4e6a-8be4-4fbde7a84723)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f19d77d6-6b6f-458c-8807-9f859ec1ee15)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3c6b7d35-ef9e-4580-8ecf-b9c863c532c3)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4f28ecc8-bab4-4c87-baa5-d521378c8074)


### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/e891803b-bdd4-4488-958f-eeceb4a2a279)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/89698a7b-b462-4351-8531-f7765c32aef2)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/4f28ecc8-bab4-4c87-baa5-d521378c8074)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f2349e1d-e942-4a93-b788-f3ac6a461b7f)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/df61a893-0675-491c-92fa-71c115f0e28c)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/ba8844cc-daa1-4d58-a03a-f6c4bce335cc)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d7d3af68-b38a-44d5-ad93-2b4c090d2ed6)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a15fee02-6363-438c-961b-43b769becd86)



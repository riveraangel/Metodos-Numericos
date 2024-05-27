# Descripción

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/dba06d37-8dc4-4403-ab22-2049552ed80c)


# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/27f6c57e-612a-4e87-a5d5-12eb5029257d)

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/7b2309e9-c5f1-47c1-83d1-91ed16840630)


# Implementación en Java

        public class Secante {
        
        public static double funcion(double x) {
            return Math.pow(x, 3) - 2;
        }
    
        public static double secante(double x0, double x1, double tolerancia) {
            double x2;
            do {
                x2 = x1 - (funcion(x1) * (x1 - x0)) / (funcion(x1) - funcion(x0));
                
                x0 = x1;
                x1 = x2;
            } while (Math.abs(funcion(x2)) >= tolerancia);
    
            return x2;
        }
    
        public static void main(String[] args) {
            double x0 = 1.0, x1 = 2.0; 
            double tolerancia = 0.0001;
            double raiz = secante(x0, x1, tolerancia);
    
            System.out.printf("La raíz es: %.4f%n", raiz);
        }
    }
    
El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d12dfb00-a978-492d-91e9-3e1749809122)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d28d8019-3a49-47a0-94fd-8f4a27698771)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a9dcde19-406e-44bb-b126-72acecb2ce28)


# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/d528e08b-5727-4cda-8b34-c02c39badebe)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c9a9742e-2e74-410b-8dbd-8aa8b168a081)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/b80fc477-75b4-4eab-b5fe-ffd536885283)


# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f056ea4f-9c45-4253-a7f0-1c6fcf11e26e)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/1705a6b4-32d8-423a-8d16-35dc909b8611)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/b271970b-6de7-4518-8c17-b780c97e543e)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/80b13fab-feb0-4e27-97c4-9a70cbaa82a2)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/c1a74a0d-6993-45ac-9d81-5ddc144f5d55)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/465f0c45-0adb-4cda-b304-a184bc59d90d)



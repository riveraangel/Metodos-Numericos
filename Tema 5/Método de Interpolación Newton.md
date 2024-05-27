# Descripción

Esta es la forma mas simple de interpolación, consiste en unir
dos puntos con una línea recta. La estrategiaes usar una línea
recta para conectar los datos conocidos a ambos lados del
punto desconocido.

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/dd0c1178-a753-4a95-8772-50410736573c)


![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/9dc69439-fc7f-405a-922a-28c6b6340f6e)


# Algoritmo

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2045ca13-62b7-4997-8304-15eb29e93e04)


# Implementación en Java
    
        public class InterpolacionNewton {
    
        public static double coeficienteNewton(double x0, double y0, double x1, double y1) {
            return (y1 - y0) / (x1 - x0);
        }
    
        public static double interpolacionNewton(double x0, double y0, double x1, double y1, double xi) {
            double a = coeficienteNewton(x0, y0, x1, y1);
            double b = y0 - a * x0;
            return a * xi + b;
        }
    
        public static void main(String[] args) {
            // Puntos de datos (x, y)
            double x0 = 0;
            double y0 = 1;
            double x1 = 2;
            double y1 = 3;
    
            double xi = 1;
    
            double yi = interpolacionNewton(x0, y0, x1, y1, xi);
            System.out.println("Valor interpolado en x = " + xi + " es y = " + yi);
        }
    }


El anterior código se utilizó para darle solución a los siguiente ejercicios. 

# Ejercicio 1

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/2b4073a5-3912-40d3-be9e-e45309a64b53)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/ab468ec3-f912-460f-8bc3-c4d045e30fb5)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/34938ee6-0470-4d11-bc3a-bfefe7f380c0)



# Ejercicio 2

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/f6bf570a-12b3-4a09-87f0-06e5bdefc7f5)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/1dff3d9f-9ca5-48ec-ab36-654f8118819e)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/5f62266d-a52f-4915-9cd9-62c46f45ec2d)

# Ejercicio 3

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/685ae367-66f3-471c-8764-c182eda8e48d)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/97eef016-c109-4b85-a00a-dd540e631585)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/3d9db0e3-bbd9-4dea-ad35-8623b9ea5acc)


# Ejercicio 4

### Problema

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/a16cd061-b7e5-48c0-9e85-529f0c060dfd)

### Solución analítica

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/31cbc287-2bc4-4453-89a8-a54e03474c11)

### Solución con código

![image](https://github.com/riveraangel/Metodos-Numericos/assets/161758059/80857513-0283-4128-a3af-e2e56b4a04ad)



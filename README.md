# Diario de una ingeniera en apuros

Hola para todos, el día de hoy vengo a mostrarles como realicé el reto #4 (uno de los retos más sufridos hasta el momento). La idea de este reto era:

1. Crear un algortimo para obtener los números primos hasta n, usando pseudocódigos y diagramas de flujo

2. Obtener un procedimiento matemático por medio del cual logremos hallar raíces cuadras, y de esta manera plantear el algoritmo en pseudocódigo junto con su respectivo digrama de flujo

## Hallando números primos
Para este caso el algoritmo propuesto es el de crear una lista hasta el número n, al mismo tiempo crear una lista J donde estarán todos los números primos (iniciando por el 2), luego de esto se irá sumando un 1 a cada número i para de esta manera dividirlo por los números que están en la lista J.
Si el residuo de la división es 0 quiere decir que no es primo pues el múltiplo de alguno de los que si son primos y si su residuo no es cero quiere decir que si es primo, por lo tanto se colocará en la lista J y este procedimiento se repetirá hasta llegar a n. Para de esta manera obtener la lista J donde estarán ubicados los números primos

```
[Variables]
i: entero
n: entero
Lista_J: Hasta n
INICIO
 ingresar_numero_n
 i=2
 Mientras (i≤n) hacer
    (i/lista J = 0) hacer
    print numero lista_J
    Si (i ∈ j) entonces (i es primo) 
 sino
    (i no es primo)
    i := i + 1
  Fin mientras
   Fin print lista_J
   FIN
```  
[![Diagrama-sin-t-tulo-Page-1.jpg](https://i.postimg.cc/2y5GjTHj/Diagrama-sin-t-tulo-Page-1.jpg)](https://postimg.cc/LYrLNkKG)

## ¿Y las raíces pa' cuando?
Bueno, pues es ahora donde comienza la parte más difícil y la que más se sufrió pero al parecer se logró o al menos eso espero.

En este caso propuse un algoritmo un poco complejo, que se compone de separar las cifras en grupos pares, de allí hallar un número cuyo cuadrado sea menor o igual al primer grupo de cifras, luego de esto elevar ese resultado al cuadrado y restar el número con el que iniciamos para de esta manera ir encontrando la raíz del número, este proceso se repite en caso de que el resultado de la diferencia no sea 0 o la cifra tenga más de 2 grupos. Pero para explicar esto mejor pues que mejor que un pseudocódigo o un diagrama de flujo, entonces menos chachara y más trabajo.

```
[variables]
n: real
p: real
q: real
z: real
raíz cuadrada: real

[INICIO]
Si (n ∈ R ) entonces
Separar n en grupos de 2 dígitos
    Si el n es impar agregar 0 al inicio de n
Buscar el mayor número cuyo cuadrado sea menor o igual al primer grupo de dos cifras
a = entero(raiz_cuadrada(groups[0]))
res = groups[0] - a**2
resultado = [a]
Repetir el proceso cuando hay 2 grupos o el resultado de la diferencia no es 0 y asi hallar decimales 
 res = res*100 + groups[i]
    x = 0
    y = 2*resultado[-1]
    mientras Verdadero:
        si (y+x)**2 <= res:
            x += 1
        sino:
            y -= 1
        si x > y:
            romper
    resultado.append(x-1)
    res = res - (x-1)**2
    Escribir raiz cuadrada con aproximacion de 3 decimales

```

Pero para hacerlo un poco más fácil de entender, diseñé el siguiente diagrama

[![Diagrama-sin-t-tulo-P-gina-2.jpg](https://i.postimg.cc/m2JTWgjJ/Diagrama-sin-t-tulo-P-gina-2.jpg)](https://postimg.cc/crRpQZVB)

Sé que es un poquito difícil de comprender pero con mucha paciencia y concetración se logra.

Espero haya logrado el objetivo del reto y que los próximos retos no sean tan difíciles para mí.

¡Muchas gracias por llegar hasta aquí y espero tengas un lindo día!

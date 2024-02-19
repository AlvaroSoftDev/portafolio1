# **PRIMER TRABAJO - PORTFOLIO EN MARKDOWN**
---
Autor: Álvaro Guerrero

Asignatura (Grado Superior): Programación (DAM)

---
![Imagen de portfolio](https://i.pinimg.com/564x/74/cc/58/74cc58b26b3c0f6475f7f3d2c369e05c.jpg)

---
## 1. ==Expectativas antes de aprender POO==
* *¿Qué creías que ibas a aprender?*
  
Personalmente, he de decir que había indagado de manera autodidacta sobre este tema antes de comenzar el Grado Superior
en el instituto. Por tanto, recordaba un poco sobre lo que iba el mismo.
Sin embargo, antes de haber escuchado o leído sobre ello, previo al inicio de estos estudios, la verdad que no tenía 
muy claro o no me imaginaba de lo que trataba la programación orientada a objetos en un principio.
Pensé que sería un apartado más dentro del aprendizaje de programación del estilo al de variables, bucles, arrays, etc.
* *¿Para qué creías que iba a servir lo que ibas a ver sobre este tema?*

Retomando y volviendo al curso en sí, y tal y como nos había adelantado el profesor a lo largo de lo que llevamos del
mismo, esta manera de programar me imaginaba que sería algo que facilitaría el mantenimiento y la estructuración del
código empleado en cualquier aplicación, la cual aunaría todo lo visto hasta el momento.

---
## 2. ==Aprendizaje==
* *¿Qué has aprendido durante las 2 unidades?*

A lo largo de estas dos unidades he podido clarificar, en primer lugar y con respecto a la POO (1ª unidad), el concepto 
de **clases**, **objetos** y la relación que tienen entre sí. Algo que es muy importante a la hora de utilizar la 
programación orientada a objetos.
En segundo lugar, y no menos importante, a definir las **propiedades** y **métodos** necesarios para que el 
programa/aplicación funcione correctamente. Cabe mencionar en este momento a los **constructores**, métodos que llevan
el nombre de la propia clase y que sirven para definir las propiedades que consideremos necesarias en la creación de un
objeto.
En relación a la POO avanzada (2ª unidad), he aprendido a distinguir las diferentes relaciones existentes entre clases:
* **Asociación**: clases cuyos objetos pueden comunicarse con objetos de otras clases.
* **Agregación**: un objeto forma parte de otro.
* **Composición**: un objeto contiene a otro (el pequeño no puede existir sin el superior).


Por otro lado, y dentro de esta misma unidad de trabajo, he aprendido el concepto de **herencia** y su representación
en notación **UML**, el cual lleva implícito en sí mismo otros dos muy importantes: **subclase y superclase**.
Aparecen en este momento también palabras importantes como:
* **Super**: que permite acceder a métodos de la clase superior cuando se ha anulado algún método.
* **Casting**: que permite cambiar un objeto a otra clase siempre que sea compatible.
* **Instanceof**: operador que devuelve verdadero si un objeto pertenece a una clase concreta.

Finalmente, aparecen otros tres conceptos que han sido realmente útiles en el aprendizaje de la POO:
* **Clase abstracta**: clase genérica que define los métodos de sus clases herederas pero sin implementarlos.
* **Interfaz**: aseguran que una clase implementa métodos concretos (ej: Escribible)
* **Clase object**: es la superclase de todas las clases en Java y todos los objetos de cualquier clase son 
descendientes de ella.

[**APUNTES** (Para más información...)](https://jorgesanchez.net/manuales/viejos/fpr/fpr0709.pdf)

---
## 3. ==Prácticas==
* *Elige los 2 ejercicios de las prácticas que consideres más importantes. ¿Por qué? ¿Qué has aprendido con ellos?*

Antes de mencionar los 2 ejercicios que, según mi opinión, han sido los más interesantes, me gustaría destacar el 
ejercicio 21. Fue un ejercicio en el que había que crear dos clases "sencillitas" (Libro y Dado), el cual me pareció muy
práctico a la hora de repasar y entender las bases y los conceptos de **clases**, **métodos** y **propiedades**.

Ahora bien, el primer ejercicio que voy a elegir, es el ejercicio número 22 (**Pilas y Colas**). Fue una práctica que me
resultó realmente interesante, lo primero, porque era algo nuevo para mí. Y en segundo lugar porque aprendí el 
funcionamiento que tienen las pilas y las colas (creación de los métodos pertinentes). 

* *¿Cómo los has resuelto?*
A continuación muestro una parte del código correspondiente a dichos métodos:

    * *Métodos push y pop de la Pila:*
```
public void push(String texto) { // Solo puedo hacer push si la pila no está llena
        if (full() == false) { // podría poner (!full())
            pila[cima] = texto;
            cima++;
        }
    }

    public String pop() {
        if (empty() == false) {
            String aux = pila[cima - 1];
            cima--;
            return aux;
        } else { // obligatorio el else, porque si no da fallo. Es un método que tiene que devolver algo siempre.
            return null;
        }
    }
```

    * *Métodos add y poll de la Cola:*

```
public void add(String nuevo) {

        if (full() == false) {
            cola[fin] = nuevo;
            fin++;
        }
    }

    public String poll() {
        if (empty() == false) {
            String res = cola[0];
            // desplazamos todos los elementos de la cola a la izquierda
            for (int i = 1; i < fin; i++) {
                cola[i - 1] = cola[i];
            }
            fin--;
            return res;
        } 
        else {
            return null;
        }
    }
```

---
## 4. ==Conclusiones==
* *¿Qué has aprendido realmente?*


* *¿Qué utilidad le ves?*


* *Di lo más positivo que has adquirido en estas 2 unidades*


* *Di lo que menos te ha gustado en estas 2 unidades*



---
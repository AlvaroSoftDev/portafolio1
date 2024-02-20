# **PRIMER TRABAJO - PORTFOLIO EN MARKDOWN**
---
***Autor:*** Álvaro Guerrero

***Asignatura (Grado Superior):*** Programación (1º DAM)

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

Ahora bien, el primer ejercicio que voy a elegir, es el ejercicio **número 22** (**Pilas y Colas**). Fue una práctica 
que me resultó realmente interesante, lo primero, porque era algo nuevo para mí. Y en segundo lugar, porque aprendí el 
funcionamiento que tienen las pilas y las colas (creación de los métodos pertinentes) en programación. 

* *¿Cómo lo has resuelto?*

En este caso comencé creando la clase Pila, declarando las propiedades correspondientes, para posteriormente comenzar
con los métodos que facilitaba la práctica. Una vez creados los métodos, procedí a crear la clase "App.java", clase 
principal la cual serviría para comprobar si lo establecido en las otras (clases) funcionaba o no.

El proceso de creación de la clase "Cola" fue el mismo que el anterior.

A continuación muestro una parte del código correspondiente a los métodos más característicos del ejercicio:

*Métodos push y pop de la Pila:*
```Java
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
*Métodos add y poll de la Cola:*
```Java
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
Por otro lado, el segundo ejercicio que me gustaría destacar es el **número 25**, relacionado con POO avanzada y la cual
trataba de los dispositivos (ordenadores y móviles) de los que dispone una empresa. Este ejercicio fue el primero que 
desarrollamos a partir del diagrama UML proporcionado por el profesor.

Uno de los aspectos por los que considero a este ejercicio importante es porque era el primero que hacíamos en el cual 
aparecían diferentes tipos de relaciones entre las clases/objetos (**herencia**, **composición** y **agregación**).

El conocer el tipo de relación entre objetos es clave a la hora de programar, ya que se hace de una manera u otra según 
sea el tipo de relación que une a dichos objetos.

* *¿Cómo lo has resuelto?*

En este caso aparecía una relación de **composición** de la cámara con el móvil (sin móvil no hay cámara), y una de
**agregación** del ordenador con la empresa (sin empresa los ordenadores siguen existiendo).

Además, había dos relaciones de **herencia**, ya que las **subclases** portátil y móvil pertenecían a la **superclase** 
ordenador (uso de la palabra "extends" en la declaración de la clase).

Una vez establecidas las relaciones, comencé a crear las clases más sencillas primero y dejé la clase "Empresa" para el 
final, la cual me complicó el ejercicio un poco y no pude terminarlo del todo.

A continuación muestro una parte del código correspondiente a los métodos más significativos del ejercicio:

*Herencia de Portátil con Ordenador:*
```Java
public class Portatil extends Ordenador {
    protected double peso;
```
*Métodos constructores de la clase Ordenador:*
```Java
public class Ordenador {
    protected int ram;
    protected int hd;
    protected String procesador;
    protected String nombre;
    protected boolean encendido = false;

    //CONSTRUCTORES
    public Ordenador(String nombre) {
        this.nombre = nombre;
        this.ram = 4;
        this.hd = 512;
        this.procesador = "i3";
    }

    public Ordenador(String nombre, int ram, int hd, String procesador) {
        this.nombre = nombre;
        this.ram = ram;
        this.hd = hd;
        this.procesador = procesador;
    }
}
```
*Clase Móvil:*
```Java
public class Movil extends Ordenador {
    private String tipo;
    private Camara camara; //Se necesita crear esta propiedad para que la variable abajo no muera

    //CONSTRUCTOR
    public Movil (String nombre, int ram, int hd, String procesador, String tipo, double apertura, 
    int megapixeles, String marca){
        super(nombre, ram, hd, procesador);
        this.tipo = tipo;
        camara = new Camara(apertura, megapixeles, marca);              
    }

    //OTROS MÉTODOS
    public void setTipo(String tipo) {
        this.tipo = tipo;
    }

    @Override
    public void escribir() {
        super.escribir();
        System.out.println("El tipo de móvil es: " + tipo);
        camara.escribir();
    }
}

```

---
## 4. ==Conclusiones==
* *¿Qué has aprendido realmente?*
    + He aprendido la diferencia que hay entre las distintas relaciones que se pueden dar entre clases (*asociación, 
agregación y composición*) y, por tanto, a entender los diagramas UML en los que dichas relaciones vienen dibujadas.
    + Como parte teórica de estas unidades, destacaría los conceptos de: *encapsulamiento, ocultación y polimorfismo*. 
Palabras que son clave para un posterior entendimiento del funcionamiento de las clases y los objetos.
    + A su vez, también he entendido y aprendido otros conceptos importantes como: herencia (*superclase-subclase*), 
clase abstracta, interfaz y clase object(*clase padre de todas las clases*).
    + Finalmente, otro punto que me gustaría resaltar en este proceso de aprendizaje, es la importancia de los 
**métodos estáticos** a la hora de programar, ya que te permiten su uso sin la necesidad de crear un objeto.

[X] Ver más información en el punto 2 (Aprendizaje).

* *¿Qué utilidad le ves?*
    + La principal utilidad que le veo a la Programación Orienta a Objetos (*POO*) es el **mantenimiento** de un 
proyecto. Al estar dividido en módulos (clases), hace que cualquier error a corregir/mejorar por el programador/a sea 
mucho más fácil de encontrar y, por tanto, la problemática de la desestructuración quede resuelta. 
    + Otro aspecto, cuanto menos relacionado con el anterior es, sin duda, la **eficiencia** a la hora de desarrollar 
una aplicación/proyecto. El hecho de esa división en módulos de la que hablaba previamente, hace que todo esté mucho más 
organizado y sea más accesible para el programador/a.

* *Di lo más positivo que has adquirido en estas 2 unidades*
    + Creo que lo más **positivo** ha sido entender el **funcionamiento** de esta metodología a la hora de programar, ya
que me permitirá organizar mi código en unidades lógicas y posiblemente reutilizables. 

* *Di lo que menos te ha gustado en estas 2 unidades*
    + Diría que no hay nada en concreto que **no** me haya gustado. Estoy intentando disfrutar la asignatura al máximo,
tratando de entender y aplicar todo lo que aprendo en el aula. Simplemente, desde mi punto de vista y tal y como diría 
nuestro profesor, me faltan **"horas de vuelo"** para familiarizarme mucho más con la programación en general.



---
---
layout: post
title: Bienvenido a mi blog
---
En un CFGS Desarrollo de Aplicaciones Web(DAW) aprenderás...

A programar en diferentes lenguajes como Java, Python, etc..

# Dentro de estos lenguajes veras..
## Python
- Uso de listas y bucles
- Leer y escribir en ficheros
- Uso de diccionarios
- Tratar bases de datos
- Tkinter
- RSS

## Java
- Aplicaciones Web y de escritorio
- Persistencia de datos
- Uso de listas y bucles
- Leer y escribir en ficheros
- Uso de hash
- JSON
- Javafx
- Tratar bases de datos
- Uso de DAO
- Uso de interfaces
- Crear tus propias clases
- SAX y DOM
- Inyeccion de dependencias(explicado mas adelante)
- Herencia


## Inyección de dependencias.

Existen dos formas genéricas, por constructor o por mutador(setter); la inyección de dependencias por constructor es cuando la creación de la instancia no depende del la clase. Y en su lugar el constructor de la clase recibe como argumento un objeto de la clase abstracta Vehículo lo que hace posible que Schumacher sea capaz de pilotar diferentes tipos de vehículos sin estar acoplado a alguno en particular.

public class Schumacher implements&nbsp;Piloto { 
   private Vehiculo vehiculo;
 
   public Persona( Vehiculo v){
      vehiculo = v;
   }
 
   @Override
   public void pilotar() {
      vehiculo.conducir();
   }
}

Otra manera de inyectar dependencias es mediante el uso de setters, lo que permite mayor flexibilidad. Ya que incluso después de que un objeto de la clase haya sido creado, se podrá asignar un vehículo diferente. Es importante remarcar que en este caso estamos trabajando con una Interfaz, y no con una clase normal, y gracias al polimorfismo el uso de una interfaz nos da la ventaja de que si a mitad de la carrera(la ejecución), decidimos que Schumacher conduzca un nuevo vehículo, entonces será posible cambiar la implementación de la dependencia utilizando un setter y de una forma muy sencilla.

public class Schumacher implements&nbsp;Piloto {
   private Vehiculo vehiculo;
 
   public Persona( Vehiculo v) {
      vehiculo = v;
   }
 
   public void setVehiculo(Vehiculo v) {
      vehiculo = v;
   }
   @Override
   public void pilotar() {
      vehiculo.conducir();
   }
}

Y aunque el ejemplo aquí mostrado se aplico a Java, el tema en general aplica en cualquier desarrollo de POO, y que nos dará una ventaja en cuanto a flexibilidad, mantenimiento y facilidad de testeo. Espero que esto les sea de utilidad, y si tienen alguna duda o comentario, pueden externarla en la sección de comentarios.

http://github/josembarreda.com - automatic!
[GitHub](http://github.com)

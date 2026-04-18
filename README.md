# TuNominaYa-POO

 Descripción del Proyecto

Este proyecto desarrolla un sistema de nómina en Java aplicando Programación Orientada a Objetos (POO).
Se implementan conceptos como **herencia, polimorfismo, clases abstractas y reutilización de código**.

El sistema fue ejecutado en un entorno en la nube usando **GitHub Codespaces**.

---

 Cómo compilar

```bash
javac TuNominaYa/*.java
```

 Cómo ejecutar

```bash
java TuNominaYa.PruebaSistemaNomina
```

---

 1. Justificación de la Herencia

La herencia permite crear nuevas clases reutilizando código de una clase padre.

En este proyecto, la clase `Empleado` contiene información general común para todos los empleados, como:

* nombre
* apellido
* número de seguro social

También contiene métodos comunes como:

* `getNombre()`
* `getApellido()`
* `getNumeroSeguroSocial()`
* `toString()`

Las clases:

* `EmpleadoAsalariado`
* `EmpleadoPorHoras`
* `EmpleadoPorComision`

heredan esas características mediante la palabra `extends`, evitando repetir código.

**Ejemplo:**

```java
public class EmpleadoPorHoras extends Empleado
```

Esto mejora el orden y mantenimiento del programa.

---
. Justificación del Polimorfismo

El polimorfismo permite usar una referencia general para manejar diferentes tipos de objetos.

En el programa aparece:

```java
empleados[i].ingresos();
```

Aunque el arreglo es de tipo `Empleado[]`, cada posición contiene un tipo distinto de empleado.

Java identifica automáticamente el objeto real y ejecuta el método correcto:

* `EmpleadoPorHoras` → calcula pago por horas
* `EmpleadoPorComision` → calcula comisión
* `EmpleadoAsalariado` → salario fijo
* `EmpleadoBaseMasComision` → salario base + comisión

Esto hace el sistema flexible y profesional.

---

 3. Herencia Múltiple en Java

Java **no permite** que una clase herede de dos o más clases al mismo tiempo.

**Ejemplo no válido:**

```java
class EstudianteEmpleado extends Estudiante, Empleado
```
¿Por qué?

Para evitar el **problema del diamante**, donde dos clases padres podrían tener métodos iguales y generar conflictos.

---
 Solución en Java

Java usa **interfaces** con la palabra:

```java
implements
```

**Ejemplo:**

```java
public class EstudianteEmpleado implements Estudiar, Trabajar
```

Así una clase puede tener múltiples comportamientos sin conflictos.

---
 Conclusión

Este proyecto demuestra cómo la Programación Orientada a Objetos permite crear software:

* organizado
* reutilizable
* escalable

mediante el uso de herencia, polimorfismo e interfaces.

---

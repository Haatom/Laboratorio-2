# CVDS-LABORATORIO 2

Integrantes: David Perez Mejia y Nicolas Camacho Hurtado

# **CREAR UN PROYECTO CON MAVEN**

### ¿Cuál es su mayor utilidad?

FALTA

### Fases de Maven

 1. **_compile_**: Genera los archivos __.class__, compilando las fuentes __.java__. No termina este en caso de que en algún __.class__ haya un error.
 2. **_test_**: Ejecuta los test automáticos de **JUnit** existentes, abortando el proceso si alguno de ellos falla.
 3. **_package_**: Genera el **.jar** con los **.class** compilados.
 4. **_install_**: Copia los **.jar** a un directorio en nuestro ordenador, permitiendo que este se pueda usar en otros proyectos **maven** en la misma máquina.
 5. **_deploy_**: Ubica una copia del **.jar** a un servidor remoto, permitiendo el acceso a este a cualquier otro proyecto **maven** que tenga acceso a ese servidor.

### ¿Para qué sirven los plugins?

> **¿Qué es un plugin?**
> 
> FALTA

### ¿Qué es y para qué sirve el repositorio central de maven?

FALTA


## ¿Cómo se crea un proyecto en Maven con ayuda de arquetipos?

Para poder crear un proyecto en maven con arquetipos es necesario:

```
mvn archetype:generate -Dfilter=maven-archetype-quickstart 
```

![Uno](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/1.PNG)

Esto nos generará un proyecto de manera interactiva, lo que después nos solicitará:

- Grupo
- Id del artefacto
- Versión
- Paquete

![Dos](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/2.PNG)


Ejecutamos el comando tree para visualizar las carpetas creadas por Maven

```
tree
```

![3](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/3.PNG)


# **AJUSTAR ALGUNAS CONFIGURACIONES EN EL PROYECTO**

Añadimos las propiedades en el archivo pom.xml

![properties](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/properties.PNG)


# **COMPILAR Y EJECUTAR**

### ¿Cual es el objetivo de package?

Basicamente es "empaquetar el proyecto" por defecto ademas de realizar la creación de un ejecutable .jar

### ¿Como se ejecuta desde la linea de comandos?

Usamos el comando siguiente:
      ```
      mvn exec.java -Dexec.mainClass="edu.eci.cvds.patterns.App"
      ```
      ![helloworld](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/helloworld.PNG)
      
### ¿Como se ejecuta desde la linea de comandos?

Para ejecutar desde la linea de comandos usamos el comando siguiente:
      ```
      mvn exec.java -Dexec.mainClass="edu.eci.cvds.patterns.App"
      ```  
Ejecutamos desde la linea de comandos con diferentes parametros, el primero solo con un nombre "Nicolas" y la segunda ejecución con nombre y apellido "David Perez".
      
![helloname](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/helloname.PNG)
      
      
# **HACER EL ESQUELETO DE LA APLICACION**
      
      
Se realiza la creación de los archivos como lo indica el laboratorio en cada una de las carpetas, como tambien el archivo ShapeFactory con el patron de diseño Fabrica (Factory).

![factory](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/factory.PNG)

Realizamos la ejecucución de la clase ShapeMain con diferentes parametros

* Sin parametros 

Podemos ver que salta la excepción indicando que es necesario incluir un parametro

![sinparametros](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/sinparametros.PNG)

* Parametro "qwerty"

Nos indica que no es un parametro valido

![qwerty](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/qwerty.PNG)

* Parametro "Pentagon"

![pentagon](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/pentagon.PNG)

* Parametro "Hexagon"

![hexagon](https://github.com/Haatom/Laboratorio-2/blob/master/Resources/hexagon.PNG)

### ¿Que es .gitignore?

El archivo .gitignore, es un archivo de texto que le dice a Git qué archivos o carpetas ignorar en un proyecto.\
Un archivo local .gitignore generalmente se coloca en el directorio raíz de un proyecto. También puedes crear un archivo global .gitignore, y cualquier entrada en ese archivo se ignorará en todos tus repositorios de Git.\
Para crear un archivo .gitignore local, crea un archivo de texto y asígnale el nombre ".gitignore" (recuerda incluir el . al principio). Luego, edita este archivo según sea necesario. Cada nueva línea debe incluir un archivo o carpeta adicional que quieras que Git lo ignore.\

* "*" se utiliza como una coincidencia comodín.
* "/" se usa para ignorar las rutas relativas al archivo .gitignore.
* "#" es usado para agregar comentarios
      
      
      






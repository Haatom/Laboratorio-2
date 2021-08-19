# CVDS-LABORATORIO 2

Integrantes: David Perez Mejia y Nicolas Camacho Hurtado

# **CREAR UN PROYECTO CON MAVEN**

### ¿Cuál es su mayor utilidad?

Facilitar la creación y gestión de proyectos de Software, basándose en el concepto de modelo de objeto de proyecto (POM).

Presenta una ventaja y es la conectividad remota a su propio repositorio, permitiendo acceso a utilidades adicionales, que solo son usadas si uno lo desea.

### Fases de Maven

 1. **_compile_**: Genera los archivos __.class__, compilando las fuentes __.java__. No termina este en caso de que en algún __.class__ haya un error.
 2. **_test_**: Ejecuta los test automáticos de **JUnit** existentes, abortando el proceso si alguno de ellos falla.
 3. **_package_**: Genera el **.jar** con los **.class** compilados.
 4. **_install_**: Copia los **.jar** a un directorio en nuestro ordenador, permitiendo que este se pueda usar en otros proyectos **maven** en la misma máquina.
 5. **_deploy_**: Ubica una copia del **.jar** a un servidor remoto, permitiendo el acceso a este a cualquier otro proyecto **maven** que tenga acceso a ese servidor.

### ¿Para qué sirven los plugins?

> **¿Qué es un plugin?**
> 
> Un Plugin es un fragmento o componente de código hecho para ampliar las funciones de un programa o de una herramienta.

### ¿Qué es y para qué sirve el repositorio central de maven?

Es un espacio público en el que se puede tanto subir como descargar plugins útiles para la comunidad.

En su página principal se puede encontrar de manera cronológica las más recientes publicaciones, aunque se pueden filtrar por categorias con un menú en la parte de la izquierda, buscando la funcionalidad que necesitemos.


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
      
      
      






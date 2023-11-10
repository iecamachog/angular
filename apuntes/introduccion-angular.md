# Instalación Angular

Para la instalación de **Angular** se debe tener:

  - Nodejs instalado, en una versión mayor a 14.20.0.

Para la instalación de Node js en windows se puede acceder desde https://nodejs.org/en/download

Para que la terminal es necesario realizar la siguiente búsqueda en windows y abrir command prompt:

![image](https://github.com/iecamachog/angular/assets/132395694/5ff84a63-158a-4990-9d90-523162c1d390)

Posterior se ingresara el siguiente comando para la instalación de Angular:

```
npm install -g @angular/cli
```

Una vez terminado el proceso crearemos **nuestro primer proyecto prueba**, para ello se ingresa el siguiente comando:

```
ng new hola-mundo-example
```
> El nombre hola-mundo-example, solo es referencia a la creación de un primer hola mundo.

Nos mostrará un mensaje, nos indica si se desea agregar el archivo **routing**, este archivo sirve para declarar las rutas o url de las vistas a un futuro,
lo conveniente es teclear **y** y Enter.

Seguido nos indica seleccionar que estilos utilizaremos, daremos enter para seleccionar los **CSS**

## Estructura de archivos.

Los primeros archivos que modificaremos están en la carpeta **app**

   - app-routing.module.ts: se administraran las rutas para la aplicación web.
   - app.component.css: Se pueden incorporar estilo de manera general, pero para mejor optimización utilizaremos otro archivo (styles.css) 
   - app.component.html: Se coloca solo la etiqueta **<router-outlet></router-outlet>**, *por default tiene código el cual se tiene que eliminar*

## Estructura al recién crear un proyecto angular

![Captura de pantalla 2023-11-10 110809](https://github.com/iecamachog/angular/assets/132395694/ea2101c7-ad7c-4d03-966d-eb0916767689)


## Ejemplo de cómo deberá quedar el archivo app.component.html

![Captura de pantalla 2023-11-10 111338](https://github.com/iecamachog/angular/assets/132395694/e58b79a0-b033-49ca-a83a-67f083b53591)


# Creación de un componente

## Un componente en angular es el conjunto de 3 archivos:

   - ejemplo.component.html : Archivo donde se ingresa la parte de vista para este componente
   - ejemplo.component.ts: Archivo que servirá para declarar métodos, variables, logica, etc...
   - ejemplo.component.css : Hoja de estilo exclusivo (por default, ya que se puede manipular) para el componente
   - ejemplo.component.spect.ts: Archivo para pruebas (Normalmente no se utiliza, se puede elimimar)

 ## Comando para la creación de un componente

Para crear el componente lo podemos hacer de manera sencilla en la terminal:

```
 ng g c nombre-componente
```

> Posible mensaje al crear el primer componente, teclear **y** y enter:
![Captura de pantalla 2023-11-10 112256](https://github.com/iecamachog/angular/assets/132395694/fc690b39-2a9c-4d66-a450-11623e75a5e8)

**Componente:**

![Captura de pantalla 2023-11-10 112613](https://github.com/iecamachog/angular/assets/132395694/df8ab606-6877-49d3-ae38-02f77d2392e4)


# Asignar ruta para observar el componente

Recordemos que tenemos un archivo para declarar rutas **app-routing.module.ts** ingresaremos el siguiente código:

```
{path:'hola-mundo', component:HolaMundoComponent}
```
La anterior línea representa que:

   - **path**: será la ruta que para ingresar a esa vista
   - **component**: El nombre del componente, este nombre lo asigna por automático y lo podemos obtener del archivo **ejemplo.component.ts**

> Recuerda importa el componente con **import { HolaMundoComponent } from './hola-mundo/hola-mundo.component';**

### El documento quedará así:
![Captura de pantalla 2023-11-10 113258](https://github.com/iecamachog/angular/assets/132395694/9112804e-dd10-482b-90f8-4a4047491049)


### Levantamos la aplicación con **ng serve**

Al tener todo correcto nos mostrará un mensaje con el puerto donde podemos acceder a la aplicación
![Captura de pantalla 2023-11-10 113430](https://github.com/iecamachog/angular/assets/132395694/16897b4e-81a8-4756-a12a-c8a993493c3e)



> En mi caso la ruta para ver el archivo será http://localhost:49225/hola-mundo
![Captura de pantalla 2023-11-10 113622](https://github.com/iecamachog/angular/assets/132395694/72fecc52-9eb5-4fbe-b4c7-3a43293a2629)

# Instalación Angular

Para la instalación de **Angular** se debe tener:

  - Nodejs instalado, en una versión mayor a 14.20.0.

Para la instalación de Node js en windows se puede acceder desde https://nodejs.org/en/download

Para que la terminal es necesario realizar la siguiente búsqueda en windows y abrir command prompt:

<img src="https://github.com/iecamachog/angular/assets/132395694/ab1c7e08-1b7c-4542-b1ac-4dd68f9653b6" width="500px" >

Posterior se ingresara el siguiente comando para la instalación de Angular:

```
npm install -g @angular/cli
```

Una vez terminado el proceso crearemos **nuestro primer proyecto prueba**, para ello se ingresa el siguiente comando:

```
ng new hola-mundo-example
```
> El nombre hola-mundo-example, solo es referencia a la creación de un primer hola mundo.

El siguiente mensaje, nos indica si se desea agregar el archivo **routing**, este archivo sirve para declarar las rutas o url de las vistas a un futuro,
lo conveniente es teclear **y** y Enter.


<img src="https://github.com/iecamachog/angular/assets/132395694/a4dc524c-cd6b-4e83-8b87-c773588a63fc" width="500px" >


Ahora nos indica seleccionar que estilos utilizaremos, daremos enter para seleccionar los **CSS**


<img src="https://github.com/iecamachog/angular/assets/132395694/b526eab9-3bba-48cc-9b89-fa33eb0f002f" width="500px" >


## Estructura de archivos.

Los primeros archivos que modificaremos están en la carpeta **app**

   - app-routing.module.ts: se administraran las rutas para la aplicación web.
   - app.component.css: Se pueden incorporar estilo de manera general, pero para mejor optimización utilizaremos otro archivo (styles.css) 
   - app.component.html: Se coloca solo la etiqueta **<router-outlet></router-outlet>**, *por default tiene código el cual se tiene que eliminar*

## Estructura al recién crear un proyecto angular

![image](https://github.com/iecamachog/angular/assets/132395694/efc1db28-6d55-4098-8f61-db3cb4f76d9a)

## Ejemplo de cómo deberá quedar el archivo app.component.html

![image](https://github.com/iecamachog/angular/assets/132395694/fb99ddf1-f622-46a3-becf-9d35e89f40f9)

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
![image](https://github.com/iecamachog/angular/assets/132395694/7906b3ae-6e76-4e35-a425-c0f98c57fdae)

**Componente:**
![image](https://github.com/iecamachog/angular/assets/132395694/ca48bf3f-0f43-4125-8916-414a76434c39)

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

![image](https://github.com/iecamachog/angular/assets/132395694/9c5663fb-5c2e-4dca-b798-4e8b8d72e433)

### Levantamos la aplicación con **ng serve**

Al tener todo correcto nos mostrará un mensaje con el puerto donde podemos acceder a la aplicación

![image](https://github.com/iecamachog/angular/assets/132395694/747f1779-129c-4b89-b9e9-91c54936d109)

> En mi caso la ruta para ver el archivo será http://localhost:49225/hola-mundo

![image](https://github.com/iecamachog/angular/assets/132395694/7b0b4854-529f-4296-84c9-391cab5e9051)

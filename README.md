# TimbaGamesPrueba

## Windows Form for visual studios 2019

##escena de creación del formulario
```c#

 partial class Form1
    {
        /// <summary>
        /// Variable del diseñador necesaria.
        /// </summary>
        private System.ComponentModel.IContainer components = null;

        /// <summary>
        /// Limpiar los recursos que se estén usando.
        /// </summary>
        /// <param name="disposing">true si los recursos administrados se deben desechar; false en caso contrario.</param>
        protected override void Dispose(bool disposing)
        {
            if (disposing && (components != null))
            {
                components.Dispose();
            }
            base.Dispose(disposing);
        }

```

CONTENIDO
1. Clases
2. Modelo
3. Figuras
4. Interfaz
5. Ejecutable
6. Manual de usuario
7. Instalación

>> para visualizar de mejor manera, abrir con un editor .md

1. Clase
   
   >> 2 clases en lenguaje C#, una de ellas, la capa de codigo de la interfaz que permite visualizar las figuras gemetricas
   >> CLASE "Class_shapes.cs" crea las figuras geometricas y las pinta en una caja para poder visualizarlas
   >> CLASE "Form1.cs" es la clase que permite controlar los comportamientos en la interfaz, viene a ser el controlador en un modelo MVC
   >> INTERFAZ "Form1.cs[diseño]" vendria a ser la interfaz.

2. Modelo
   
   >> El desarrollo fue creado por medio del framework de windows form de visual studios, totalmente por codigo y sin motores graficos del mercado

3. Figuras 
    
    >> Cuadrado
    >> Circulo
    >> Triangulo
    >> Hexagono
   
 4. Interfaz
 
   ![image](https://user-images.githubusercontent.com/70168236/135383987-c38868c7-5dda-402d-97d7-b4ed2abf7f68.png)

 
 5. Ejecutable

    >> descargar de este repositorio
 
 6. Manual de usuario
 
    >> en la interfaz, se mostraran 7 botones, 4 son las figuras geometricas, al presionarlas, ellas saldran en el recuadro de espacio en blanco. Los otros botones son para la direccion de inzquierda a derecha, de arriba hacia abajo y el movimiento en forma de caja, por ultimo un boton que detenga el proceso.

    >> los botones de las figuras estaran en la parte inferior izquierda del formulario y los de movimientos en la parte inferior derecha, el de boton que permite detener los proceso (stop) se ubica en la parte superior derecha.
 
 7. Instalacion 
 
 ![image](https://user-images.githubusercontent.com/70168236/135385495-b2118e7c-7218-4b8c-b715-9baf6d3346ae.png)

    >> en la carpeta comprimida donde salen los archviso de codigo, esta el ejecutable dentro de otra carpeta con el nombre "publish", en el recuadro rojo, da doble clcik para abrir e instalar la aplicación.
    
    





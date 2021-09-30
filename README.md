# TestingCodeTimba

## Windows Form for visual studios 2019

##Nicolás Stevens Parra Redondo - Test Code Timba Games

CONTENIDO
>> 1. Instalación
>> 2. Modelo
>> 3. Figuras
>> 4. Clases
>> 5. Interfaz y Animación
>> 6. Manual de usuario

1. Instalación
   
   >> Para la instalación del programa se debe seguir los siguientes pasos:
   >> 1. Descomprimir la carpeta TestigCodeTimba en cualquier parte del computador.
   >> 2. Abrir la carpeta TestingCodeTimba la cual tendrá 3 archivos.
   >> 3. Ejecutar el archivo "setup" para la instalación del programa.
   >> 4. Dar clic en instalar y esperar a que el programa abra.

2. Modelo
   
   >> Toda la solución fue hecho en el lenguaje de programación C# usando Visual Studio 2019 para su desarrollo y ejecución de prueba.
   >> No se utilizó ningun programa externo, ni ayuda de motores graficos por requerimientos de la prueba.
   >> Se tomaron en cuenta ciertas librerias para el desarrollo:
   ```c#
        using System.Windows.Forms;
        using System.Drawing;
   ```
   >> Se uso el framework de Windows Form en ayuda de la creación y animación de las distintas figuras requeridas.

3. Figuras 
    >> Las figuras requeridas para la prueba fueron las siguientes:
    >> Cuadrado
    >> Circulo
    >> Triangulo
    >> Hexagono
   
 4. Clases
 
   >> Se creó una clase llamada Class_Graphics.cs para el dibujado de las figuras usando las librerias.
   >> Se llama a la clase Graphics para el dibujado y se maneja por un arreglo llamado Point para el trazado de poligonos.
   ```c#
       using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Drawing;

namespace TestingCodeTimba
{
    class Class_Graphics
    {
        Graphics shapes;
        Point[] punto = new Point[6];
        Point[] triangle = new Point[3];
        Pen pen = new Pen(Color.Red);

        public void Square(PictureBox cuadro)
        {
            cuadro.Refresh();
            shapes = cuadro.CreateGraphics();

            shapes.DrawRectangle(pen, 0, 0, 50, 50);
        }

        public void Circle(PictureBox cuadro)
        {
            cuadro.Refresh();
            shapes = cuadro.CreateGraphics();

            shapes.DrawEllipse(pen, 0, 0, 50, 50);
        }

        public void Triangle(PictureBox cuadro)
        {
            cuadro.Refresh();
            shapes = cuadro.CreateGraphics();
            triangle[0] = new Point(0, 30);
            triangle[1] = new Point(60, 30);
            triangle[2] = new Point(30, 0);

            shapes.DrawPolygon(pen, triangle);
        }

        public void Hexagon(PictureBox cuadro)
        {
            cuadro.Refresh();
            shapes = cuadro.CreateGraphics();
            punto[0] = new Point(10, 0);
            punto[1] = new Point(0, 10);
            punto[2] = new Point(10, 20);
            punto[3] = new Point(30, 20);
            punto[4] = new Point(40, 10);
            punto[5] = new Point(30, 0);

            shapes.DrawPolygon(pen, punto);
        }
    }
}  
   ```
   >> La clase donde se encuentra la interfaz y la logica de la animación se realizó en la clase por defecto llamada Form1.cs.
   >> La logica de animación funciona con la herramienta de los Timer la cual ejecutan las acciones en determinados tiempos de intevalo en los ejes X Y.
   >> Se agregaron botones para llamar los eventos del dibujado de las figuras, las animaciones y el "Stop" de las mismas.
   

 
 5. Interfaz y Animación

    >> Para la interfaz se manejó el Formulario por defecto
    >> Contiene 8 botones en total (4 que dibujan las figuras, 3 para las animaciones y 1 para detener dichas animaciones)
    >> Se encuentra un Picturebox1 para poder mostrar las imagenes codificadas de las figuras y poder manipularlas de mejor manera
    >> Logicamente contiene 3 Timer para las animaciones las cuales se mueven el Picturebox para mejor estabilidad y menor complejidad ( up/Down, Left/Right y Box), no se pudo realizar la animación en circular por problemas técnicos.
    >> Todas las funcionalidades estan los botones.
 
 6. Manual de usuario
 
    >> Al abrir el programa se encontrará un formulario con 8 botones en total.
    >> Dibujar primero las figuras antes de ejecutar las animaciones:

    >> Al lado inferior izquierdo se encontrarán 4 botones asignados para dibujar las figuras ( dar clic en los diferentes botones de figuras para visualizarlas).
    >> Al lado inferior derecho estaran 3 botones que ejecutan las distintas animaciones, cualquier figura puede ser animada.
    >> En centro inferior estará el botón para detener cualquier animación en proceso, esto deshabilitará cualquier Timer
    

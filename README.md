# Tarea-3_VLSI
Esta tarea se cetrará en la instanciación y caracterización de un flip flip estático Amo-Esclavo de 1 bit, utilizando la herramienta de Custom Compiler. El objetivo principal es validar el comportamiento eléctrico del flip flop mediante simualciones detallas y comparaciones con los datos del fabricante. Estos procesos son de suma importancia para asegurar fiabilidad y el rendimiento de los sistemas digitales.
## Parte 1.
Primeramente, se realiazaron las intancias en el Custom Compiler de lo que es el equematico y el trazado del flip flop estático Amo-Esclavo de 1 bit, se adjunta las evidencias en las siguientes imágenes.
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/8cb61afa-1b4a-4020-a1e9-c7fe0c90b375" width="500"  /><br>
     <em>Esquematico del flip flop Amo-Esclavo de 1 bit</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/0dcacbeb-ed65-4807-9a45-b2adfd48a3e4" width="500"  /><br>
     <em>Layout del flip flop Amo-Esclavo de 1 bit</em>
</p>

<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/304c6e0f-92da-47a2-b3f3-f8dcfb3b44a5" width="500"  /><br>
     <em>Post-trazado con parásitas del flip flop Amo-Esclavo de 1 bit</em>
</p>

## Parte 2.
Seguidamente se implementó lo que sería una señal de reloj utilizando la fuente de pulsos, para simular un reloj real. Debido a que es una señal sin retardos, se le colocaron 2 inversores con un tamaño de 1X y 4X. De esta manera se hace una simulación realista de lo que es una pendiente de clk a las entradas del flip flop. Se adjuntan las evidencias en las siguientes imágenes.
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/3f00d393-24fd-4d62-bddb-0c47f4dcbec5" width="500"  /><br>
     <em>Flip flop con entradas y salidas</em>
</p>

## Parte 3.
Para esta parte se debe realizar una comparación de datos simulados con los datos provistos por el fabricante. Utilizando Liberty Displayer, se obtuvieron las características eléctricas del flip flop. Una vez teniendo el reloj listo, se implementaron una serie de simulaciones que nos permitieron determinar y comparar los datos provistos por el fabricante. Adémas se le incoroporó una carga a la salida de F04 con inversores mínimos. Se adjunta la tabla comparativa y las imágenes de las simulaciones.

Para las simulaciones, el reloj tuvo una pendiente de 39.8 ps. Según los datos del fabricante, los valores de hold y setup deberían determinarse dentro del rango de pendiente de 14 ps a 1120 ps.
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/b9ce5a79-710d-4fdb-a0f3-cbde6e72499d" width="500"  /><br>
     <em>Pendiente del clock</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/1262b192-d5f5-4e53-8128-6ac78fc99f62" width="500"  /><br>
     <em>Tiempo de setup D to CN (rise)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/30c49f8e-a8eb-43be-be57-e18caa99bef4" width="500"  /><br>
     <em>Error de setup D to CN (rise)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/181784e1-559a-4c3a-8166-895e5b2df348" width="500"  /><br>
     <em>Tiempo de setup D to CN (fall)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/91cbf82a-d2a5-4e86-b0bf-7c785a909c95" width="500"  /><br>
     <em>Error de setup D to CN (fall)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/8ed13544-c84d-4e71-b5c0-16c162ed9ead" width="500"  /><br>
     <em>Tiempo de hold D to CN (rise)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/386b0b01-6eb2-4d39-89c0-ada4798df49c" width="500"  /><br>
     <em>Error de hold D to CN (rise)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/ad048a3e-ba93-4615-bbbb-b690070121b0" width="500"  /><br>
     <em>Tiempo de hold D to CN (fall)</em>
</p>
<p float="center">
  <img src="https://github.com/Rmarino25/Tarea-3_VLSI/assets/110353604/42958e28-a69b-4d02-b8ad-ca04ea47ed8f" width="500"  /><br>
     <em>Error de hold D to CN (fall)</em>
</p>

En la siguiente tabla se hace una comparación de los datos simulados con los provistos por fabricante.

| Tiempo                         | Fabricante [ns]       | Simulado [ps] |
|--------------------------------|-----------------------|---------------|
| Setup D to CN (rise)           | [-0.338 a 0.106] ns   | 96.4 ps        |
| Setup D to CN (fall)           | [0.023  a 0.221] ns   | 227 ps        |
| Hold D to CN (rise)            | [0.135  a 0.529] ns   | 114 ps        |
| Hold D to CN (fall)            | [-0.137 a 0.104] ns   | 115 ps        |


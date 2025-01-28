La página es pública y se accede desde https://l0g6.github.io/Contaz/ 

Este código
trata de crear una forma 
rápida de contabilizar ocurrencias de
un rango de cifras. EL rango por defecto
será de [1..26].
Se deberán tener los botones con la cifra y al pulsarlos
se incrementará el contador asociado.
El último contador incrementado quedará con un fondo
distintivo y sólo este.
Existirá un botón para ordenar los contadores en base al número del contador y otro para ordenarlos en base a su cifra.
Actualizaciones.
Vamos a crear una segunda finalidad del código. Guardar en un archivo de texto lo que se va pulsando. Cada botón pulsado se guarda como lo que indica su valor. Por ejemplo si se pulsa el botón 1 y luego el 27 se escribirán en el archivo de texto como 1 27. Se separan por un espacio. Por otro lado se añadirán los siguientes botones como si fueran teclas de signos de puntuación. Una tecla para espacio . Cuando se pulse añadirá un espacio. Otras teclas para los siguientes símbolos ! " [ ] ; , : .  El punto es una de las teclas. En la tecla de espacio se mostrará como Space. El nombre con que se guardará el texto será CodificadoAAMMDDHHMMSS.txt donde AA es el año DD es el día HH es la hora MM es el minuto y SS los segundos.  Las pulsaciones se irán viendo en una caja de texto que tendrá un botón guardar para que se escriba a archivo. Espero que quede clara la idea. 
Los botones añadidos como Espacio y signos de puntuación no serán contabilizados.
Cada vez que se pulsa un botón se previsualiza en una caja de texto y luego cuando se pulse el botón Guardar se guarda con el nombre predefinido (dar opción de poner otro nombre)
Voy a implementar los cambios que solicitaste, añadiendo la funcionalidad de guardar las pulsaciones en un archivo de texto con las características que describiste. Esto incluye:

Botones adicionales para los signos de puntuación y espacio, los cuales no serán contabilizados.
Una caja de texto donde se previsualizan las pulsaciones.
Un botón para guardar el contenido de la caja de texto en un archivo .txt con un nombre predeterminado basado en la fecha y hora.
La posibilidad de cambiar el nombre del archivo antes de guardarlo.

He añadido la funcionalidad para guardar las pulsaciones en un archivo de texto, junto con los botones de signos de puntuación y espacio. También se incluye una caja de texto para previsualizar las pulsaciones y un formulario para guardar el archivo con un nombre predeterminado basado en la fecha y hora o un nombre personalizado.
He agregado la funcionalidad para deshacer la última pulsación. Esto incluye:

Botón de Backspace: Se agregó un botón con el carácter gráfico de "←" (flecha de retroceso).
Decremento de contador: Cuando se usa Backspace, se resta 1 al contador del último botón pulsado.
Iluminación: Después de deshacer, se ilumina el nuevo último botón pulsado.
Previsualización ajustada: Se actualiza la caja de texto eliminando el último carácter.
Falla cuando se introduce ". Probar.
Falla al borrar un número. Corregir

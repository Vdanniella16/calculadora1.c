# calculadora1.c
**Variables:** 
primer_digito, segundo_digito, operacion: Almacenan los números y el resultado de la operación.
val: Variable temporal que almacena el valor de la tecla presionada.
funcion: Variable que indica en qué fase se encuentra el programa: obteniendo el primer dígito, el segundo dígito o realizando una operación.

Funciones:
```main():```
Función principal del código. Llama a las funciones de inicialización y luego entra en un bucle infinito donde se espera la presión de teclas y se realiza la operación de la calculadora.
inicializar():

Configura los puertos GPIO para el uso de los pines de entrada y salida.
configuracion_teclado():

Configura los pines GPIO necesarios para el teclado matricial.
tecla_presionada():

Comprueba qué tecla del teclado matricial ha sido presionada y realiza acciones según la tecla presionada.
imprimir_bcd_decodificador_7_segmentos(uint8_t val):

Imprime el valor pasado como argumento en el display de siete segmentos. Esta función también actualiza el estado del programa dependiendo de la fase en la que se encuentre.
demoraMs(int n):

Crea una demora de aproximadamente n milisegundos.
Flujo de Programa:
Inicialización:

Configuración de pines GPIO para el teclado y el display.
Bucle Principal:

Espera la presión de una tecla.
Cuando se presiona una tecla, determina la acción a realizar.
Si es un número, lo almacena en val.
Si es una operación de suma, resta o multiplicación, realiza la operación correspondiente con los valores almacenados en primer_digito y segundo_digito.
Actualiza el display con el resultado de la operación.

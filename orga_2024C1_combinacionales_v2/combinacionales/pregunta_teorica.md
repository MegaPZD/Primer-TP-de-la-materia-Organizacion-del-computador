# Respuesta a la pregunta Teorica:
## "¿Qué operaciones hace este circuito (inversor_4)
##  sobre el numero B?"

Los resultados de las operaciones a la entrada A, salientes
por S dependerán del **MULTIPLEXOR** asi que comencemos explicando
que hace este en el circuito:

El multiplexor tiene una linea de control **INV** de un bit  funcionará
como el accionador el multiplexor, funcionando este como interruptor;
- Sí INV es 0 la entrada de datos seleccionada será la O y la salida del
  multiplexor tendrá el valor que el numero entrante.
- En cambio, sí INV es 1 la entrada será la 1 y la salida corresponderá
  a el numero entrante posterior a las operaciones.

## Camino 1: el entrante con INV = 0

- En este caso no se le realizarán modificaciones a A y la salida S
  corresponderá a su valor.

## Camino 2: el entrante con INV = 1

- Se empieza con invertir la totalidad de los bits de A
- El resultado de la inversión entrará por el **incrementador_4**
  donde se le sumará 1 (un) bit mediante el **sumador_4** y el resultado
  (sin importar el cout) es el que pasará por la entrada del
  multiplexor
- Como en este camino INV es igual a 1 la salida S tendrá como valor
  el resultado de las operaciones de los items anteriores.

## Excepciones:

- Por como funciona el circuito habrá numeros que aunque INV = 1
  el resultado de la inversión será el mismo numero de la entrada B
- **0000**: Se invierte = 1111, se le suma 1 = 0000, salida S = **0000**

- **1000**: Se invierte = 0111, se le suma 1 = 1000, salida S = **1000**
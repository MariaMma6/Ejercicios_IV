#Ejercicios tema 1: Introducci�n a la infraestructura virtual: concepto y soporte f�sico

**EJERCICIO 1** :Consultar en el cat�logo de alguna tienda de inform�tica el precio de un ordenador tipo servidor y calcular su coste de 
amortizaci�n a cuatro y siete a�os.

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-1.PNG " ")

*AMORTIZACI�N A 4 A�OS*
Sabiendo que se aplica un 25% del precio total

Primer a�o : 2.809,90� x 0.25 = 702,47�
Segundo a�o: 2.809,90� x 0.25 = 702,47�
Tercer a�o : 2.809,90� x 0.25 = 702,47�
Cuarto a�o : 2.809,90� x 0.25 = 702,47�


*AMORTIZACI�N A LOS 7 A�OS*
Sabiendo que se amortiza m�s los primeros a�os y dicha amortizaci�n va reduci�ndose con el paso de los a�os.

Primer a�o : 2.809,90� x 0.25 = 702,47�
Segundo a�o: 2.809,90� x 0.25 = 702,47�
Tercer a�o : 2.809,90� * 0.15 = 421,48� 
Cuarto a�o : 2.809,90� * 0.15 = 421,48� 
Quinto a�o : 2.809,90� * 0.10 = 280,99� 
Sexto  a�o : 2.809,90� * 0.05 = 140,49�
S�ptimo a�o: 2.809,90� * 0.05 = 140,49�


**EJERCICIO 2**: Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, Comparar el 
coste durante un a�o de un ordenador con un procesador est�ndar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) 
y con el resto de las caracter�sticas similares (tama�o de disco duro equivalente a transferencia de disco duro) en el caso de que la 
infraestructura comprada se usa s�lo el 1% o el 10% del tiempo.

Como servidor dedicado he elegido Acens, servidor dedicado acens SERVER 16.
*SERVIDOR DEDICADO*![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-2.PNG " ")

Para el servicio en la nube he elegido Microsoft Azure Est�ndar A3.
*SERVICIO EN LA NUBE*
![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-3.PNG " ")


Con un uso de 1%:

-Servidor dedicado   :  99,90  �/mes * 12 meses  = 1198,8 euros/a�o. 
-Servicio en la nube : (225,87 �/mes * 12 meses) * 0.01 = 27,10 euros/mes.

Con un uso de 10%:

-Servidor dedicado   :  99,90  �/mes * 12 meses  = 1198,8 euros/a�o. 
-Servicio en la nube : (225,87 �/mes * 12 meses) * 0.10 = 271,04 euros/mes.


**EJERCICIO 3**: �Qu� tipo de virtualizaci�n usar�as en cada caso?

- Virtualizaci�n plena: nos proporciona la ventaja de poseer varios SO en un mismo ordenador de forma aislada entre ellos, adem�s de ello, nuestro SO anfitri�n se encuentra seguro e independiente del resto de sistemas operativos. Ejemplo: VMWare o VirtualBox.
- Virtualizaci�n parcial: Utilizado con el fin de compartir recursos entre varios usuarios, haciendo creer a cadauno de ellos que poseen el recurso en su totalidad.
- Virtualizaci�n de aplicaciones: �til para un caso en que queramos utilizar una aplicaci�n de un sistema operativo (Windows por ejemplo), en otro sistema operativo (Linux por ejemplo) que no posee dicha aplicaci�n.
- Virtualizaci�n de entornos de desarrollo: En caso de querer realizar comprobar el funcionamiento de aplicaciones en diferentes entornos.

**EJERCICIO 4**: Comprobar si el procesador o procesadores instalados tienen estos flags. �Qu� modelo de procesador es? �Qu� aparece como salida de esa orden?

Para ver el modelo de procesador utilizaremos la siguiente orden:

	cat /proc/cpuinfo

Como salida obtenemos:

	Intel(R) Core(TM) i5-4210U CPU @2.70 GHz

Para visualizar los flags usaremos la siguiente orden:

	egrep '^flags.*(vmx|svm)' /proc/cpuinfo

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-5.PNG " ")

**EJERCICIO 5.1**: Comprobar si el n�cleo instalado en tu ordenador contiene este m�dulo del kernel usando la orden kvm-ok.

Instalamos kvm mediante la siguiente orden:

	sudo apt-get install cpu-checker

Y seguidamente ejecutamos:

	sudo kvm-ok

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-5.PNG " ")


**EJERCICIO 5.2**: Instalar un hipervisor para gestionar m�quinas virtuales, que m�s adelante se podr� usar en pruebas y ejercicios.

Ya tengo instalado VirtualBox.
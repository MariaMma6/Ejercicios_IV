#Ejercicios tema 1: Introducción a la infraestructura virtual: concepto y soporte físico

**EJERCICIO 1** :Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de 
amortización a cuatro y siete años.

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-1.PNG " ")

**AMORTIZACIÓN A 4 AÑOS**
*Sabiendo que se aplica un 25% del precio total*

Primer año : 2.809,90€ x 0.25 = 702,47€
Segundo año: 2.809,90€ x 0.25 = 702,47€
Tercer año : 2.809,90€ x 0.25 = 702,47€
Cuarto año : 2.809,90€ x 0.25 = 702,47€


**AMORTIZACIÓN A LOS 7 AÑOS**
*Sabiendo que se amortiza más los primeros años y dicha amortización va reduciéndose con el paso de los años.*

Primer año : 2.809,90€ x 0.25 = 702,47€
Segundo año: 2.809,90€ x 0.25 = 702,47€
Tercer año : 2.809,90€ * 0.15 = 421,48€ 
Cuarto año : 2.809,90€ * 0.15 = 421,48€ 
Quinto año : 2.809,90€ * 0.10 = 280,99€ 
Sexto  año : 2.809,90€ * 0.05 = 140,49€
Séptimo año: 2.809,90€ * 0.05 = 140,49€


**EJERCICIO 2**: Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, Comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.

Como servidor dedicado he elegido Acens, servidor dedicado acens SERVER 16.

**SERVIDOR DEDICADO**

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-2.PNG " ")

Para el servicio en la nube he elegido Microsoft Azure Estándar A3.

**SERVICIO EN LA NUBE**

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-3.PNG " ")

Con un uso de 1%:

-Servidor dedicado   :  99,90  €/mes * 12 meses  = 1198,8 euros/año. 
-Servicio en la nube : (225,87 €/mes * 12 meses) * 0.01 = 27,10 euros/mes.

Con un uso de 10%:

-Servidor dedicado   :  99,90  €/mes * 12 meses  = 1198,8 euros/año. 
-Servicio en la nube : (225,87 €/mes * 12 meses) * 0.10 = 271,04 euros/mes.


**EJERCICIO 3**: ¿Qué tipo de virtualización usarías en cada caso?

- Virtualización plena: nos proporciona la ventaja de poseer varios SO en un mismo ordenador de forma aislada entre ellos, además de ello, nuestro SO anfitrión se encuentra seguro e independiente del resto de sistemas operativos. Ejemplo: VMWare o VirtualBox.
- Virtualización parcial: Utilizado con el fin de compartir recursos entre varios usuarios, haciendo creer a cadauno de ellos que poseen el recurso en su totalidad.
- Virtualización de aplicaciones: Útil para un caso en que queramos utilizar una aplicación de un sistema operativo (Windows por ejemplo), en otro sistema operativo (Linux por ejemplo) que no posee dicha aplicación.
- Virtualización de entornos de desarrollo: En caso de querer realizar comprobar el funcionamiento de aplicaciones en diferentes entornos.

**EJERCICIO 4**: Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?

Para ver el modelo de procesador utilizaremos la siguiente orden:

	cat /proc/cpuinfo

Como salida obtenemos:

	Intel(R) Core(TM) i5-4210U CPU @2.70 GHz

Para visualizar los flags usaremos la siguiente orden:

	egrep '^flags.*(vmx|svm)' /proc/cpuinfo

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-5.PNG " ")

**EJERCICIO 5.1**: Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.

Instalamos kvm mediante la siguiente orden:

	sudo apt-get install cpu-checker

Y seguidamente ejecutamos:

	sudo kvm-ok

![img] (https://github.com/MariaMma6/IV/blob/hito1/imagenes/P1-5.PNG " ")


**EJERCICIO 5.2**: Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.

Ya tengo instalado VirtualBox.

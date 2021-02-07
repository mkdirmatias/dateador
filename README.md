# Dateador
Este script se construyó a base de distintas conexiones que se lograron obtener en servicios públicos del estado, las vulnerabilidades fueron reportadas hace mucho tiempo atrás, pero no hubo respuesta alguna y aún siguen vigentes.

La lista de servicios vulnerados son los siguientes:

- **ISPCH**
    - Esta información se logró obtener de dos formas, a través de un servicio usado por un hospital público, el cual cuando se realizaba la atención, los datos del paciente se ingresaban delante del mismo, y el paciente es capaz de ver la pantalla. Bastó con memorizar la ip la cual estaba expuesta a internet y no de forma local (tiene lógica, ya que no es un servicio privado) y la contraseña usada por el médico la cual era un número de 3 dígitos. Al analizar el sitio, se encontró el uso de una api totalmente expuesta sin ningún método de seguridad la cual nos lleva a la según forma de obtener esta información, ya sabiendo el dominio, con el uso de google dorks se lograba encontrar dicha api (cosa que hoy en día ya no es posible). La api realiza una conexión solo con el rut del paciente y devuelve información personal del mismo.

- **SII**
    - Si bien esta información es de carácter público, se automatizó el proceso para hacer bypass al captcha, por lo que basta solamente tener el rut de la persona y se puede conocer su situación tributaria.

- **SRCEI** y **FONASA**
    - Ambos sitios cuentan con la misma vulnerabilidad la cual consiste en un mal manejo del sistema de Clave Única, lo que permite consultar ruts de forma deliberada sin ningún tipo de validación previa.

    Por parte del SRCEI se logra obtener información actualizada y de carácter privado del rut consultado, por otro lado, si la persona está adscrita a FONASA, se logra obtener detalle de sus atenciones médicas.


# Screenshots

![https://i.imgur.com/GFFWJoZ.png](https://i.imgur.com/GFFWJoZ.png)
![https://i.imgur.com/kbPAPYf.png](https://i.imgur.com/kbPAPYf.png)
![https://i.imgur.com/C6SImcx.png](https://i.imgur.com/C6SImcx.png)

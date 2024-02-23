# Sistema de Transporte en Java

Este repositorio contiene una aplicación Java diseñada para gestionar el envío de paquetes utilizando diferentes tipos de transporte.

## Descripción

La aplicación permite calcular el coste de envío y determinar el tipo de embalaje necesario para un paquete, en función del tipo de transporte utilizado. Actualmente, la aplicación soporta el envío por camión y bicicleta.

## Funcionalidades

- Cálculo del coste de envío basado en el código postal de destino.
- Determinación del tipo de embalaje en función del peso y las dimensiones del paquete.

## Uso

Para utilizar la aplicación, debes instanciar la clase de transporte que deseas utilizar (por ejemplo, Camion o Bicicleta). A continuación, puedes llamar a los métodos costeTotal(int cp) y tipoEmbalaje(float x, float y, float z, float peso) para calcular el coste de envío y determinar el tipo de embalaje, respectivamente.

## Ejemplo

```java
Camion c = new Camion();
Bicicleta b = new Bicicleta();
Factory f = new Factory();

int codigoPostal = 12345;
float costeCamion = c.costeTotal(codigoPostal);
int embalajeCamion = c.tipoEmbalaje(60.0f, 60.0f, 60.0f, 30.0f);
float costeBicicleta = b.costeTotal(codigoPostal);
int embalajeBicicleta = b.tipoEmbalaje(30.0f, 30.0f, 30.0f, 5.0f);

System.out.println("Coste total para envío en camión: $" + costeCamion);
System.out.println("Tipo de embalaje para envío en camión: " + f.getProducto(embalajeCamion));
System.out.println("Coste total para envío en bicicleta: $" + costeBicicleta);
System.out.println("Tipo de embalaje para envío en bicicleta: " + f.getProducto(embalajeBicicleta));
```
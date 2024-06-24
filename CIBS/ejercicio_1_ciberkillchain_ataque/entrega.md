# Ejercicio CiberKillChain - Ataque

### Alumna: María Antonella Crestan

## Sistema víctima
*Trabajo Final de Especialización de Ing. Luciano Matías Ciminari Smith*: **Sistema de monitoreo para puntos de venta** [link](https://lse-posgrados-files.fi.uba.ar/tesis/LSE-FIUBA-Trabajo-Final-CEIoT-Luciano-Matias-Ciminari-Smith-2022.pdf).

El trabajo consiste en la instalación de estantes inteligentes en locales comerciales. Estos podrían detectar los cambios en el stock de productos, a través de sensores de peso que tienen en su interior. El beneficio del producto, entre otros, es que la información que reporta puede ser usada por los dueños del comercio y los proveedores de productos para entender así los patrones de consumo, nivel de stock y requerimientos de abastecimiento. 

![image](https://github.com/AntonellaCrestan/ceiot_base/assets/141678982/77440134-58e7-40e5-bd60-14a10ca9abbe)

"Arquitectura del Sistema"- Fuente: Trabajo Final Ing Ciminari Smith

## Sistema ataque
### Objetivo
Como parte de la competencia en el rubro de estantes inteligentes, mi objetivo es que la aplicación del frontend muestre datos erróneos manipulados, volviendo el producto poco fiable e indeseable para los usuarios, tanto los dueños de los comercios como proveedores de los productos. 
### Resolución
**FASE I**
 1. **Reconnaissance**:
   -	Recolecto información sobre los locales comerciales que tienen instalado los estantes inteligentes a partir de la red social LinkedIn del fabricante, donde tiene expuesto quiénes son sus clientes. [Technique 1593.001](https://attack.mitre.org/techniques/T1593/001/).
2. **Weaponization**:
  - **Decido** armar un discurso para convencer a los clientes de que deben compartirme su usuario y contraseña para poder corregir errores del backend en la aplicación de sus sensores. Les transmito la urgencia de que el error implica que se carguen costos adicionales a su tarjeta de crédito por cada toma de dato. 
3. **Delivery**:
  - Me comunico telefónicamente con los clientes con el discurso ya preparado. Es suficiente con la obtención de los datos de 1 cliente.   [Technique 1598.004](https://attack.mitre.org/techniques/T1598/004/)
4. **Exploitation**
  -	Un cliente comparte su usuario y contraseña.
5. **Installation**
  -	Ingreso a la aplicación del usuario y avanzo con la segunda fase del ataque:

**FASE 2**
1. **Reconnaissance**:
   -	Accedo a la aplicación del producto e investigo vulnerabilidades para poder adulterar los datos que tiene almacenado el sistema. [Technique 1595.002](https://attack.mitre.org/techniques/T1595/002/)
2. **Weaponization**:
  -	**Decido** desarrollar un malware capaz de controlar los sensores remotos que estén conectados a la aplicación del cliente y alterar los valores que presenten. [Technique 1587.001]( https://attack.mitre.org/techniques/T1587/001/)
     - La alteración de los valores no debe ser fácilmente perceptible, con el objetivo de que las fallas en el conteo del stock se relacionen a un mal funcionamiento del estante IoT comprado y no a fallas de la aplicación.
  - **Decido** escribir un e-mail marketing que invite a descargar una actualización de la aplicación para tener el último ajuste en cuanto a tolerancia de mediciones de los sensores y conexión con los proveedores de productos.
3. **Delivery**:
  -	Envío el malware como adjunto en el correo electrónico que escribí.  
4. **Exploitation**
  -	Los clientes descargan y ejecutan el malware recibido. [Technique 1203](https://attack.mitre.org/techniques/T1203/)
5. **Installation**
  -	El malware se instala en la computadora personal del usuario y acciona en segundo plano. 
6. **Command & Control**
  - Cuando el usuario ingrese a la aplicación del estante IoT el malware está programado para ejecutar cambios en la base de la aplicación. 
7. **Actions on Objectives**
  - Al interferir en la programación base de la aplicación, se logra que en cada valor del dashboard final exista una diferencia porcentual de 5% con lo real. Esta variación porcentual cambia cada semana.
  - Mantengo las alteraciones en valores hasta que el cliente decida desinstalar los estantes inteligentes que tiene en su local comercial. Teniendo la información de contacto del cliente le ofrezco los estantes inteligentes que yo fabrico. 

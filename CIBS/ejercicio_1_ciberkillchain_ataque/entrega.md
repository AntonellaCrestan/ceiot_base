# Ejercicio CiberKillChain - Ataque

### Alumno: María Antonella Crestan

## Sistema víctima
*Trabajo Final de Especialización de Ing. Luciano Matías Ciminari Smith*: **Sistema de monitoreo para puntos de venta** [link](https://lse-posgrados-files.fi.uba.ar/tesis/LSE-FIUBA-Trabajo-Final-CEIoT-Luciano-Matias-Ciminari-Smith-2022.pdf).

El trabajo consiste en la instalación de estantes inteligentes en locales comerciales. Estos podrían detectar los cambios en el stock de productos, a través de sensores de peso que tienen en su interior. El beneficio del producto, entre otros, es que la información que reporta puede ser usada por los dueños del comercio y los proveedores de productos para entender así los patrones de consumo, nivel de stock y requerimientos de abastecimiento. 

![image](https://github.com/AntonellaCrestan/ceiot_base/assets/141678982/77440134-58e7-40e5-bd60-14a10ca9abbe)

"Arquitectura del Sistema"- Fuente: Trabajo Final Ing Ciminari Smith

## Sistema ataque
### Objetivo
Como parte de la competencia en el rubro de estantes inteligentes, mi objetivo es que la aplicación del frontend muestre datos erróneos manipulados, volviendo el producto poco fiable e indeseable para los usuarios, tanto los dueños de los comercios como proveedores de los productos. 
### Resolución
 1. **Reconnaissance**:
   -	Recolecto información sobre los locales comerciales que tienen instalado los estantes inteligentes a partir de la red social LinkedIn del fabricante, donde tiene expuesto quiénes son sus clientes. [Technique 1593.001](https://attack.mitre.org/techniques/T1593/001/).
   -	Me comunico telefónicamente con los clientes alegando problemas en el registro de los datos desde los sensores, y solicito usuario y contraseña para poder repararlos. Es suficiente con la obtención de los datos de 1 cliente.   [Technique 1598.004](https://attack.mitre.org/techniques/T1598/004/)
   -	Accedo a la aplicación del producto e investigo vulnerabilidades para poder adulterar los datos que tiene almacenado el sistema. [Technique 1595.002](https://attack.mitre.org/techniques/T1595/002/)
2. **Weaponization**:
  -	**Decido** desarrollar un malware capaz de controlar los sensores remotos que estén conectados a la aplicación del cliente y alterar los valores que presenten. [Technique 1587.001]( https://attack.mitre.org/techniques/T1587/001/)
     - La alteración de los valores no debe ser fácilmente perceptible, con el objetivo de que las fallas en el conteo del stock se relacionen a un mal funcionamiento del producto comprado y no a fallas de la aplicación. 
3. **Delivery**:
  -	Envío el malware como adjunto en un correo electrónico. Invito a los clientes a descargarlo como actualización de la aplicación para tener el último ajuste en cuanto a tolerancia de mediciones y conexión con los proveedores de productos.
4. **Exploitation**
  -	Los clientes descargan el malware recibido. [Technique 1203](https://attack.mitre.org/techniques/T1203/)
5. **Installation**
  -	El malware se instala interfiriendo en los datos que recolectan los sensores. 
6. **Command & Control**
  -	Controlar las modificaciones que se realicen sobre la aplicación para conocer si deja de aplicarse la modificación de valores. [Technique 1219](https://attack.mitre.org/techniques/T1219/)
7. **Actions on Objectives**
  - Mantengo las alteraciones en valores hasta que el cliente decida desinstalar los estantes inteligentes que tiene en su local comercial. Teniendo la información de contacto del cliente le ofrezco los estantes inteligentes que yo fabrico. 

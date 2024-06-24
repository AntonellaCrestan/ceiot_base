# Ejercicio CiberKillChain - Defensa

### Alumna: María Antonella Crestan

## Sistema defensa

## Enunciado

Desarrollar la defensa en función del ataque planteado en orden inverso, mencionar una medida de detección y una de mitigación, sólo lo más importante, considerar recursos limitados. No es una respuesta a un incidente, hay que detectar el ataque independientemente de la etapa.

## Resolución Defensa Fase II
1. **Actions on Objectives**
  - Detección: ante comentarios de los clientes sobre el inconveniente en las mediciones. Los dueños de locales comerciales generarían compras innecesarias y los proveedores de productos no podrían obtener información fidedigna sobre la forma de consumo.
  - Mitigación: auditar los archivos que se ejecutan junto con la aplicación del producto en las computadoras de los clientes. Para así detectar anomalías en el funcionamiento. [Mitigation 1047](https://attack.mitre.org/mitigations/M1047/)
2. **Command & Control**
  - Detección: Detecto movimientos de stock en días donde el local comercial se encuentra cerrado. 
  - Mitigación: auditar los archivos que se ejecutan junto con la aplicación del producto en las computadoras de los clientes. Para así detectar anomalías en el funcionamiento. [Mitigation 1047](https://attack.mitre.org/mitigations/M1047/)
3. **Installation**
  - Detección:La aplicación se ejecuta con archivos en segundo plano que alteran su funcionamiento y velocidad habitual 
  - Mitigación: Configurar la aplicación para que no pueda ejecutar un archivo desconocido en su interior. [Mitigation 1038](https://attack.mitre.org/mitigations/M1038/)
4. **Exploitation**
  -	Mitigación: Informar a los usuarios que no deben instalar ningún nuevo archivo para la ejecución de la aplicación, e insistir en desestimar correos no oficiales.
5. **Delivery**:
  - Detección: un cliente consulta sobre el correo electrónico recibido.
  - Mitigación: Informar a todos los usuarios que no deben instalar ningún nuevo archivo para la ejecución de la aplicación, e insistir en desestimar correos no oficiales. [Mitigation 1017](https://attack.mitre.org/mitigations/M1017/)
6. **Weaponization**:
  -	Detección: la aplicación recibe un tráfico inusual e identifico vulnerabilidades en que cada usuario puede ingresar a la configuración total del sistema.
  -	Mitigación: Cambio los permisos de cada usuario para que no puedan ver todos los detalles de la programación del producto. [Mitigation 1024](https://attack.mitre.org/mitigations/M1024/)
 7. **Reconnaissance**:
  - Detección: la aplicación recibe un tráfico inusual e identifico vulnerabilidades en que cada usuario puede ingresar a la configuración total del sistema.
  - Mitigación: Incorporar nuevo proceso de autenticación por token, que se recibe en el número telefónico entregado al iniciar sesión en un nuevo dispositivo. [Mitigation 1032](https://attack.mitre.org/mitigations/M1032/)



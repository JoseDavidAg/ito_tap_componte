# Temporary-Password-Generator

## Descripción
Este componente no visual en Java permite generar contraseñas temporales y enviarlas por correo electrónico a los usuarios. Está diseñado para manejar situaciones comunes en las que los usuarios olvidan sus contraseñas, proporcionando una solución segura y eficiente para la recuperación de acceso.

El componente se basa en la generación de tokens temporales, los cuales almacenan la contraseña temporal, los datos del correo electrónico del usuario y el nombre del usuario. Estos tokens aseguran que la contraseña temporal es válida y no ha expirado antes de permitir el acceso.

## Usos
1. **Aplicaciones de Gestión de Usuarios:** Ideal para sistemas donde los usuarios necesitan recuperar el acceso a sus cuentas olvidadas, permitiendo una integración sencilla y segura de la funcionalidad de restablecimiento de contraseñas. 
2. **Herramientas de Seguridad:** Puede ser parte de una suite de seguridad, asegurando que las contraseñas temporales cumplen con los requisitos de seguridad, como los establecidos en RFC 4086: Randomness Requirements for Security.
3. **Aplicaciones Web y Móviles:** Adecuado para aplicaciones que manejan información sensible y requieren un alto nivel de seguridad en la recuperación de contraseñas, como plataformas bancarias, de comercio electrónico, entre otras.
4. **Herramientas de Desarrollo de Software:** Útil para desarrolladores que necesiten implementar la funcionalidad de recuperación de contraseñas en sus aplicaciones, ofreciendo una solución personalizada que maneja datos persistentes en archivos de texto.

## Características
* Generación de Contraseñas Temporales.
* Validación de Tokens.
* Envío de Correos Electrónicos.
* Persistencia de Datos.

## Requisitos*
* Java JDK 8 o superior.
* Librerías de correo electrónico para Java (JavaMail API).
* Librerías de Activation Framework 1.1.1
* Este componente está diseñado para ser flexible y fácilmente integrable en diversas aplicaciones Java, proporcionando una solución robusta y segura para la recuperación de contraseñas mediante el uso de tokens temporales.

## API
### TemporaryPassword
#### Descripción
  La clase `TemporaryPassword` es la unica clase que debera ser instanciada por el programador. Su propósito principal es generar y gestionar contraseñas temporales, asegurando una implementación limpia y legible dentro del paquete.
  
#### Métodos

| Nombre | Tipo de Dato que Retorna | Tipo de dato que recibe | Descripción |
|--------|--------|-------------------------|-------------|
| `start` | void | String correo | Verifica que correo cumpla los requisitos de un correo, obtiene una contraseña segura y crear un `TokenService`. Por ultimo envia un correo con la contraseña temporal al correo proporcionado.|

---


### TokenService
#### Descripción
  La clase TokenService ofrece servicios de utilidad relacionados con la creación y validación de tokens temporales. Estos tokens se utilizan para permitir el acceso temporal a usuarios y proporcionar una forma segura de recuperación de contraseñas. El TokenService facilita tanto a los usuarios como a los programadores la generación y verificación de tokens dentro de sus programas.
#### Métodos

| Nombre | Tipo de Dato que Retorna | Tipo de dato que recibe | Descripción |
|--------|--------|-------------------------|-------------|
| `crearToken` | void | String correo, String password| Crea un `Token` con el correo de recuperacion, la contraseña generada y un tiempo de 5 minutos de vigencia despues de ser creada, obtiene el nombre del usuario relacionada al correo y almacena los datos en  una ruta de archivo.  |
| `isValidToken` | boolean | String usuario, String contraseña | Verifica que el usario tenga un Token vigente y que se haya proporcionado la contraseña correcta|

---


### Utileria
#### Descripción
#### Campos
#### Constructores
#### Métodos

### Validacion
**Descripción**
**Campos**
**Constructores**
**Métodos**

### Constantes
#### Descripción
#### Campos
#### Constructores
#### Métodos


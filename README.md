# Embedded-PaymentForm-T1.Net

Ejemplo del formulario incrustado de Izipay con C# .NET, para poder ejecutar el siguiente ejemplo seguir los pasos del presente manual.

![pagar](images/pagar.png)

## Requisitos Previos

* Instalar Visual Studio [Aquí](https://visualstudio.microsoft.com/es/)
* Version de .NET CORE de 3 en adelante
* Extraer credenciales del Back Office Vendedor. [Guía Aquí](https://github.com/izipay-pe/obtener-credenciales-de-conexion)

## 1.- Descargar
Descargar el proyecto .zip haciendo click [Aquí](https://github.com/izipay-pe/Embedded-PaymentForm-T1-React/archive/refs/heads/main.zip) o clonarlo desde Git.
```sh
git clone https://github.com/izipay-pe/Embedded-PaymentForm-T1.Net.git
``` 

## 2.- Obtener Claves
* Obtener claves de integración, [Ver ejemplo](https://github.com/izipay-pe/obtener-credenciales-de-conexion#readme)
 
## 3.- Configurar claves
* Obtener claves de API REST desde guía de integración ver [Requisitos Previos](#Requisitos_Previos).
* Editar el archivo `PaymentModel.cs` con las claves de su Back Office Vendedor
```html
        //Usuario
        private const string _usuario = "XXXXXXXXXXXXXXXXX";
        //Clave API REST de TEST o PRODUCCIÓN
        private const string _contraseña = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        //Clave JavaScript de TEST o PRODUCCIÓN
        private const string _clave_JS = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        //Clave HMAC-SHA-256 de TEST o PRODUCCIÓN
        private const string _clave_SHA256 = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
        //URL de servidor de IZIPAY
        private const string _servidor_API = "https://api.micuentaweb.pe/";

``` 
![Claves](images/credenciales.png)

## 4.- Correr Proyecto
* IIS Express
* Correr proyecto con el Explorador Web de su preferencia

## 5.- Implementar IPN

* Ver manual de implementacion de la IPN [Aquí](https://secure.micuentaweb.pe/doc/es-PE/rest/V4.0/kb/payment_done.html)
* Ver el ejemplo de la respuesta IPN [Aquí](https://github.com/izipay-pe/Redirect-PaymentForm-IpnT1-PHP)

## 6.- Demo
![demo](images/demo.png)

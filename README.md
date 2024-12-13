# Agenda de Contactos

Este proyecto es una aplicación web de agenda de contactos que permite a múltiples usuarios gestionar sus contactos, enviar mensajes y mantener un registro de las interacciones. La aplicación está desarrollada en PHP y utiliza MySQL como base de datos.

## Características

- **Registro y Login**: Los usuarios pueden registrarse con un número de teléfono y contraseña, y acceder a su cuenta.
- **Gestión de Contactos**: Los usuarios pueden agregar, buscar y ver detalles de sus contactos.
- **Mensajería**: Los usuarios pueden enviar mensajes a sus contactos y ver el historial de mensajes.
- **Interfaz Intuitiva**: La aplicación cuenta con una interfaz sencilla y fácil de usar.

## Lenguajes Utilizados

- PHP
- MySQL
- HTML/CSS

## Estructura del Proyecto

| Archivo                   | Descripción                                                  |
|--------------------------|--------------------------------------------------------------|
| `index.php`              | Página principal con la lista de contactos                   |
| `login.php`              | Página de inicio de sesión                                   |
| `registro.php`           | Página de registro de nuevos usuarios                        |
| `detalles.php`           | Página que muestra los detalles del contacto y permite enviar mensajes |
| `cerrarSesion.php`       | Página que informa que se ha cerrado la sesión              |
| `conexion.php`           | Función que establece la conexión con la Base de Datos      |
| `usuariosService.php`    | Funciones de gestión de usuarios                             |
| `contactosService.php`   | Funciones de gestión de contactos                            |
| `mensajesService.php`    | Funciones de gestión de mensajes                             |
| `usuario.php`            | La clase usuario                                            |
| `contacto.php`           | La clase contacto                                           |
| `mensaje.php`            | La clase mensaje                                           |
| `estilos.css`            | Archivo CSS para los estilos                                |

## Ejemplo de función: conexionBD() 

```php
function conexionBD() {
    $host = 'localhost';
    $usuario = 'root';
    $password = '';
    $basededatos = 'migtd4';

    $conexion = new mysqli($host, $usuario, $password, $basededatos);

    if ($conexion->connect_error) {
        echo 'nanai de la china';
        die('la has cagao chaval');
    }
    return $conexion;
}
```
## Consideración con las fotos de perfil

En caso de que en los formularios del usuario o del contacto no se haya subido una imagen, se les asignaará como avatar/foto la siguiente imagen 

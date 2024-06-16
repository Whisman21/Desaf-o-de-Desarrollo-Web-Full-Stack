# Desafio-de-Desarrollo-Web-Full-Stack
Esta api esta orientada a un sistema para la gestión de productos y usuarios de un negocio, para poder probarla correctamente se debe de instalar los siguientes paquetes si no se tienen:

System.data.sqlclient
Newtonsoft.Json
BCrypt.Net-Next
Microsoft.AspNetCore.Authentication.JwtBearer
Microsoft.EntityFrameworkCore.Tools
Swashbuckle.AspNetCore.Swagger

La api debe de ejecutarse en modo https 
![image](https://github.com/Whisman21/Desaf-o-de-Desarrollo-Web-Full-Stack/assets/144621111/8273d5d7-23b1-49a3-bfd0-8977ae654b53)

En la Clase "Conexion.cs" debera de poner sus datos correspondientes a su base de datos 
public static string cadenaConexion = "Data Source=(nombre del server);Initial Catalog=(Nombre de la base de datos);User ID=(nombre de usuario);Password=(clave)";

Funcionalidades de las Api:
- Obtener todos los productos.
- Obtener un producto por su ID.
- Obtener un producto por su nombre o desc
- Agregar un nuevo producto.
- Actualizar un producto existente.
- Eliminar un producto por su ID.
- Obtener todos los Usuarios.
- Obtener un usuario por su id.
- Registrar un usuario
- Hacer login
- Generar un token de ese login (Lamentablemente no funciona)
- Actualizar a un usuario
- Eliminar a un usuario

(swagger tiene unos candados que serian usados para la validacion del token y rol del usuario, pero el token generado es invalido)

Para cada funcion debera de llenar sus espacions correspondientes o le saltara error

ejemplo:
Como deberia de ser:
![image](https://github.com/Whisman21/Desaf-o-de-Desarrollo-Web-Full-Stack/assets/144621111/d04329b7-a545-49f9-af69-645f232b97b7)

Lo que pasaria si deja algo vacio (En algunos casos saldra un error directo):
![image](https://github.com/Whisman21/Desaf-o-de-Desarrollo-Web-Full-Stack/assets/144621111/38efc1de-86ae-4ad1-8a28-f2d58346096a)

Todos los Usuarios seran creados con el rol de usuario, Esto puede cambiarlo en el apartado de Actualizar usuario

Los ID son auto incrementables por lo cual cada vez que cree un usuario/producto, estos ID iran incrementandose, si llega a eliminar a un usuario/objeto y vuelve a agregar otro el id de este seguire el incremento es decir, no volvera a ser el 1

Los cambios realizados pueden ser visto en tiempo real en la misma pagina web como en la base de datos

Puede usar datos como:
Producto:
Nombre = manzana
Descripcion = Roja
Precio = 60
Stock = 70

o para usuarios
Usuario:
Nombre = Whisman
Email = Whisman@hotmail.com
Contrasena = 12345 (la contrasena sera hasheada dentro del codigo, se puede verificar si entra a la base de datos luego de agregar al usuario)











# Guia de Instalación en visual studio code

<li>
Asegúrese de que tiene instalado .NET 8.0 mediante la ejecución del siguiente comando en el terminal de comandos que prefiera:
</li>

```CLI de .NET
dotnet --list-sdks
```
<li>
Para configurar un proyecto de .NET para que funcione con API web se usa Visual Studio Code. Visual Studio Code incluye un terminal integrado que facilita la creación de un proyecto. Si no quiere usar un editor de código, puede ejecutar los comandos de este módulo en un terminal.
</li>

```CLI de .NET
dotnet new webapi -controllers -f net8.0
```

El comando usa una plantilla de proyecto de ASP.NET Core con el alias webapi, para aplicar scaffolding a un proyecto de API web basado en C#. Se crea un directorio ContosoPizza. Este directorio contiene un proyecto ASP.NET Core que se ejecuta en .NET. El nombre del proyecto coincide con el nombre del directorio ContosoPizza.

# Compilación y prueba de la API web
<li>
Ejecute el comando siguiente de la CLI de .NET Core en el shell de comandos:.
</li>

```CLI de .NET
dotnet run
```
# Exploración con archivos .http
En el proyecto se incluye ContosoPizza.http, un archivo que se usa para probar los puntos de conexión de API a través de un formato estándar. Los archivos .http se admiten en varios IDE, incluidos Visual Studio y dentro de Visual Studio Code con la extensión de cliente REST instalada.

Abra el archivo ContosoPizza.http.

Este archivo se ha configurado previamente con las variables de @ContosoPizza_HostAddress y un comando GET que llama a /weatherforecast/ que acepta application/json.

Seleccione el comando Sent Request encima de GET, que enviará una solicitud al servicio en ejecución.

Al llamar a este comando, se abrirá una ventana de respuesta con una salida similar a la que vimos en el explorador:

```CLI de .NET
HTTP/1.1 200 OK
Connection: close
Content-Type: application/json; charset=utf-8
Date: Wed, 17 Jan 2024 16:46:40 GMT
Server: Kestrel
Transfer-Encoding: chunked

[
    {
        "date": "2024-01-18",
        "temperatureC": -2,
        "temperatureF": 29,
        "summary": "Warm"
    },
    {
        "date": "2024-01-19",
        "temperatureC": 24,
        "temperatureF": 75,
        "summary": "Chilly"
    },
    // ..
]
```

# Adición de un almacén de datos
Necesita una clase model para representar una pizza en el inventario. El modelo contiene propiedades que representan las características de una pizza. El modelo se usa para pasar datos en la API web y para conservar opciones de pizza en el almacén de datos.

Ese almacén de datos es un servicio de almacenamiento en caché en memoria local simple. En una aplicación real se consideraría el uso de una base de datos, como <b>SQL Server </b>, con <b>Entity Framework Core </b>.

# Generando carpeta Models (Creación de un modelo de pizza)
<li>
Creación de un modelo de pizza
</li>

```CLI de .NET
mkdir Models
```
La raíz del proyecto ahora contiene un directorio Models con un archivo Pizza.cs vacío. El nombre del directorio Models es una convención. El nombre del directorio procede de la arquitectura Modelo-Vista-Controlador que usa la API web.

# Incorporación de un servicio de datos
Tendra que crear una carperta de nombre services y agregar una clase llamada PizzaService.cs 





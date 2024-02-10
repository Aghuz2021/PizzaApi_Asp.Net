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

# Guia de Instalación en visual studio code

<li>
Asegúrese de que tiene instalado .NET 8.0 mediante la ejecución del siguiente comando en el terminal de comandos que prefiera:
</li>

``````CLI de .NET
dotnet --list-sdks

<li>
Para configurar un proyecto de .NET para que funcione con API web se usa Visual Studio Code. Visual Studio Code incluye un terminal integrado que facilita la creación de un proyecto. Si no quiere usar un editor de código, puede ejecutar los comandos de este módulo en un terminal.
</li>

``````C#
dotnet new webapi -controllers -f net8.0

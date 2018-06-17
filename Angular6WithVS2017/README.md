# Angular6WithVS2017

Trabajar con Angular 6 en Visual Studio 2017.

## Requerimientos

- [.NET Core](https://www.microsoft.com/net/download/)
- [Node.js](https://nodejs.org/es/)
- [Angular CLI](https://cli.angular.io)

## Configuración

1. Crear una aplicación web ASP.NET Core (plantilla API)

2. En el directorio de la solución VS, ejecutar `ng new [nombre del proyecto]

3. Editar el archivo `.csproj` añadiendo las siguiente línas en la sección `PropertyGroup`

```xml
<TypeScriptCompileBlocked>true</TypeScriptCompileBlocked> 
<PostBuildEvent>ng build --aot</PostBuildEvent>
```

4. Editar el archivo `angular.json` y especificar el valor `wwwroot` en la propiedad `outpathPath`

5. En el archivo `Startup.cs` agregar dos middlewares en el método `Configure`

```
app.UseDefaultFiles();
app.UseStaticFiles();
```

6. Quitar `"launchUrl": "api/values"` del archivo **Properties/launchSettings.json**

7. Por último, al compilar y ejecutar la aplicación se mostrará la página principal de una aplicación Angular 6.

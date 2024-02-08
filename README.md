<div align="center">

# Proyecto Estimation Tool
</div>

## Guía de Instalación de IntelliJ y JDK

1. Instalar el IDE de desarrollo IntelliJ:
- **Windows**: [Descargar](https://www.jetbrains.com/idea/download/?section=windows) y seguir las instrucciones del instalador.
- **Mac**: [Descargar](https://www.jetbrains.com/idea/download/?section=mac), abrir el archivo `.dmg`, y arrastrar IntelliJ al directorio de Aplicaciones.
- **Linux**: [Descargar](https://www.jetbrains.com/idea/download/?section=linux), descomprimir el archivo y ejecutar `bin/.sh` para iniciar la instalación.  

2. Configurar IntelliJ y el JDK
  - Al iniciar IntelliJ por primera vez, se puede configurar el IDE según se prefiera. Si no se está seguro, se pueden aceptar las configuraciones predeterminadas.
  - Cuando se cree un nuevo proyecto (File > New > Project...), IntelliJ solicitará que se configure el JDK si no detecta ninguno en el sistema.
  - En el diálogo de configuración del proyecto, se verá una opción para descargar y configurar automáticamente el JDK. Seleccionar para que IntelliJ se encargue de la instalación. (Se pueden elegir entre varias versiones del JDK. Se recomienda usar la versión más reciente que sea compatible con el proyecto `JDK 21`).
  - IntelliJ descargará e instalará el JDK seleccionado, y lo configurará automáticamente para el proyecto.

3. Verificar la Instalación
Una vez completada la instalación, se puede verificar la configuración del JDK en IntelliJ yendo a File > Project Structure > Project. Aquí se podrá ver el JDK que IntelliJ ha configurado para el proyecto.


## Crear el proyecto de SpringBoot
Al iniciar IntelliJ va a aparecer una interfaz como la siguiente:
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Interfaz%20inicial%20IntelliJ.png)
</div>

1. Dar click en el botón `New Project`, aparecerá la siguiente ventana:
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Interfaz%20New%20Project.png)
</div>

2. En la seccion `Generators` que está en la columna derecha seleccionar `Spring Initializr`, ahora la ventana se verá de la siguiente manera:
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Interfaz%20New%20Project%20Spring%20Initializr.png)
</div>

3. Llenar las configuraciones del proyecto como en la siguiente imagen (La ubicación de la carpeta del proyecto es a preferencia de cada persona)
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Gu%C3%ADa%20configuraci%C3%B3n%20proyecto.png)
</div>

4. Dar click en el botón `Next`, aparecerá la ventana de gestión de dependecias de SpringBoot:
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Dependencias%20Spring%20Boot.png)
</div>

4. Seleccionar las siguientes dependencias:
<div align="center">

| Sección | Dependencias |
| --- | --- |
| Developer Tools | `Spring Boot DevTools` `Lombook` |
| Web | `Spring Web` |
</div>

5. Dar click en `Create` y aparecerá la interfaz principal del proyecto:
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Proyecto.png)
</div>

6. Abrir el archivo `pom.xml` y dentro de la etiqueta `Dependencies` agregar la siguiente dependencia
```xml
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.17.0</version>
</dependency>
```

7. Dar click en el botón que aparece con una `m` de color azul o presionar las teclas `Ctrl+Mayús+O` para guardar los cambios y cargar las dependencias al proyecto
<div align="center">
  
![App Screenshot](https://github.com/Cristian-Infante/Proyecto-Estimation-Tool/blob/CFIC/Cargar%20dependencias.png)
</div>

### Dependecias del proyecto

- Spring Boot DevTools: Proporciona herramientas útiles para el desarrollo de aplicaciones Spring Boot, como reinicio automático para reflejar cambios en el código sin necesidad de reiniciar el servidor.
- Spring Boot Starter Web: Ofrece todas las dependencias necesarias para crear aplicaciones web y servicios RESTful, incluyendo el servidor embebido Tomcat.
- Spring Boot Starter Test: Incluye soporte para pruebas unitarias y de integración con JUnit, Mockito, y otras bibliotecas útiles para testing.
- Selenium Java: Permite automatizar navegadores para pruebas de interfaces de usuario, ideal para verificar el comportamiento de aplicaciones web.
- Lombook: Proporciona anotaciones para minimizar el código repetitivo en Java, como getters, setters, y constructores, mejorando la legibilidad y reduciendo el texto repetitivo.

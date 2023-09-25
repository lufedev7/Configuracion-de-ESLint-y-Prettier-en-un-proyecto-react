 # Configuración de Eslint y Prettier en un proyecto react
ESLint y Prettier son dos herramientas poderosas que pueden mejorar significativamente la calidad y el formato del código. Mientras que ESLint se centra en mejorar la calidad del código haciendo cumplir los estándares de codificación e identificando posibles errores o problemas, Prettier se encarga específicamente del formato del código.  
Un problema importante que surge cuando varios desarrolladores tienen diferentes estilos de formato es el problema de los "cambios fantasmas". Esto se refiere a situaciones en las que los cambios de código realizados por un desarrollador pueden provocar cambios innecesarios e irrelevantes en el formato cuando los ve otro desarrollador. Para abordar este problema, es fundamental establecer reglas de formato comunes que todos los desarrolladores puedan seguir.  
Para personalizar las reglas de ESLint y Prettier, puede modificar sus archivos de configuración. Para Prettier, puede crear un archivo .prettierrc en el directorio raíz del proyecto para definir preferencias de formato específicas. Prettier puede corregir automáticamente ciertos errores, como sangrías inconsistentes o saltos de línea. Esta característica no solo ahorra tiempo, sino que también garantiza un código coherente y legible en todo el proyecto.  
Explorar diferentes configuraciones de estilo es esencial para encontrar la configuración óptima para su proyecto. Se recomienda utilizar el paquete "eslint-config-prettier" para evitar conflictos entre ESLint y Prettier. Esta configuración deshabilita cualquier regla de ESLint que pueda entrar en conflicto con el formato de Prettier. Al combinar estas dos herramientas, puede lograr un código consistente y bien formateado.  
Configurar Prettier es simple y directo. Puede instalarlo como una dependencia de desarrollo usando npm. Además, optimizar la configuración de ESLint en el archivo package.json puede excluir ciertos archivos o directorios del linting. Esto es útil cuando desea evitar dañar bibliotecas de terceros o código generado.  
Aunque configurar ESLint y Prettier puede parecer complicado al principio, es un proceso directo y esencial que mejora enormemente la calidad y el mantenimiento del código. Al seguir las mejores prácticas y establecer reglas de formato comunes, se asegura de que todos los desarrolladores que trabajan en el proyecto cumplan con los mismos estándares de codificación.  
## Si utilizas Nextjs:
Es preferible que crees el proyecto sin la configuración inicial por defecto que te genera Nextjs para ello lo puedes hacer de la siguiente manera.  
### 1. Crear el proyecto Nextjs  
Inicia un nuevo proyecto Next.js sin la configuración predeterminada de ESLint.  
### npx create-next-app   my-next-app --typescript  
### cd my-next-app    
## Configurar ESLint
Antes de empezar a codificar, es recomendable configurar ESLint.  Esta configuración es aplicable para todo proyecto que este realizado en react, independiente del framework que utilices, si utilizas nextjs te daremos ciertos pasos extras para un correcto funcionamiento de eslint.  
 Instala ESLint como una dependencia de desarrollo:  
### npm i eslint -D  
Luego, inicializa ESLint:  
### npx eslint --init  
El comando **npx eslint --init** inicia el asistente de configuración de ESLint. El asistente te hará una serie de preguntas para ayudarte a configurar ESLint para tu proyecto.
Los pasos del asistente son los siguientes:  
### 1.	¿Cómo quieres usar ESLint?  
El asistente te preguntará cómo quieres usar ESLint. Puedes elegir entre las siguientes opciones:  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/10505360-b646-4f35-a7e4-d0870b09c885)  
Para verificar la sintaxis y encontrar problemas. Esta es la opción predeterminada. ESLint verificará la sintaxis de tu código y te avisará de cualquier error o problema.  
Para verificar la sintaxis, encontrar problemas y aplicar reglas de estilo. Esta opción es más completa que la anterior. ESLint verificará la sintaxis de tu código, te avisará de cualquier error o problema y aplicará reglas de estilo para mejorar la legibilidad y mantenibilidad de tu código, en nuestro caso esa es la opción que aplicamos. 
## 2.	¿Qué tipo de módulos usa tu proyecto?  
El asistente te preguntará qué tipo de módulos usa tu proyecto. Puedes elegir entre las siguientes opciones:  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/1ae99f48-b05f-453f-83bd-9e4ed1f2a89f)  
Nosotros aplicamos Módulos JavaScript (import/export). Esta es la opción predeterminada. ESLint utilizará la sintaxis de módulos JavaScript para analizar tu código.  
## 3.	¿Qué marco de trabajo usa tu proyecto?  
El asistente te preguntará qué marco de trabajo usa tu proyecto. Puedes elegir entre las siguientes opciones:  

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/dbdce167-9051-4ff3-8c7f-645b2273e7d0)  
Debes elegir el que deseas trabajar en tu proyecto, aquí aplicaremos React. ESLint aplicará reglas específicas de React para mejorar la calidad de tu código React.  

## 4.	Definir si utilizas JavaScript o TypeScript 
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/3bb5aedf-c936-4796-8a6a-d89c4bb88cb2)  

## 5.	Especificar el entorno en donde se ejecutará tu código   

Al especificar los entornos en los que se ejecutará tu código, ESLint podrá aplicar reglas específicas del entorno para mejorar la calidad de tu código. Por ejemplo, ESLint puede evitar que uses variables globales que no están disponibles en el entorno en el que se ejecutará tu código.  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/77517538-31bf-4c20-8b32-3b7138366e85)  
En nuestro caso aplicamos en los dos entornos, para seleccionarlos utilizamos la tecla “a” así se marcan los dos.  
## 6.	Definir las guías de estilo para tu proyecto  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/c96ef0cc-bccd-47ec-8fbd-0c1bc1f34b7d)  

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/3c0a5356-49c0-4982-b610-4fc822ddf3c7)  

En nuestro caso definimos una guía popular como lo es la estándar  
## 7.	Elegir el formato en como queremos el archivo de configuración de eslint  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/838d2e65-30b8-48bc-85f8-4a1ac2bcf7b3)    
Existen tres formas de elegir el tipo de archivo para la configuración de eslint, es decisión propia escoger el formato adecuado para tu proyecto.  
## 8.	Instalar todas las dependencias y plugins para el correcto funcionamiento de eslint   

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/069a4bcd-20d2-430d-a444-737fde8ef3bc)  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/80f3a4c9-7736-42ef-9f66-5199083de371)  
Durante la inicialización, selecciona las opciones que se ajusten a tus necesidades. Elige las opciones `browser` y `node`, y cuando se te pida el estilo de código, opta por `standard`. Finalmente, instala cualquier dependencia sugerida.  
Si te encuentras con errores al ejecutar npx eslint ., puedes corregirlos agregando configuraciones adicionales a tu archivo ESLint. Por ejemplo, al usar TypeScript, es posible que necesites configuraciones adicionales.  
Si estas trabajando solo con JavaScript la configuración de eslint estaría completa, para comprobarla ejecuta el comando npx eslint . y en consola podrás Verificar todos los errores: ESLint puede identificar errores de sintaxis y otros problemas potenciales en el código JavaScript. Esto puede ayudar a prevenir errores en tiempo de ejecución y hacer que el código sea más confiable.    
## Configurar ESLint para TypeScript (Si estas utilizando TypeScript) 
Generalmente, cuando estas utilizando un proyecto con TypeScript al momento de realizar la configuración principal de eslint, suelen generarse algunos errores para solucionarlos y que ESLint funcione correctamente con TypeScript toca hacer unas configuraciones adicionales, asegúrate de tener las configuraciones adecuadas en tu archivo .eslintrc o similar.  
1.	Se debe agregar La opción **“Project”: “./tsconfig.json”** en el objeto parserOptions de la configuración de ESLint, esta le dice al analizador de ESLint que use el archivo de configuración de TypeScript especificado para obtener información sobre el tipo de los archivos que está analizando. Esto es importante para que ESLint pueda aplicar correctamente las reglas que requieren información de tipo.  
Si no especifica la opción Project, ESLint analizará todos los archivos JavaScript y TypeScript como si fueran código de tipo any. Esto significa que ESLint no podrá aplicar correctamente las reglas que requieren información de tipo.
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/07b47e88-d83a-49e7-8aec-bfd18992fc77)  
2.	En el archivo de configuración de tsconfig.json incluimos el archivo de configuración de eslint .eslintrc.js para para asegurarse de que ESLint pueda analizar todos los archivos de su proyecto  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/de3dd6e5-0d7b-46d6-b63d-f95481b1e29a)
si estas utilizando a vite como framework debes realizar otras configuraciones extras para que la eslint funcione correctamente.  
Al include le debes de agregar el archivo de configuración de vite.config.ts que es un archivo extra para la configuración con vite.
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/b266fcde-2515-468f-aab8-7e5e4aff8377)  
Otro error que puedes presentar utilizando vite es que te pide que especifiques la versión de react en el archivo de configuración de eslint para ello debes de agregarlo   


![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/cd42c8f7-ef7d-425a-a525-0ab8b81935e9)  
La versión de react es de acuerdo a tu proyecto, esta la puedes ver en el archivo de package.json   
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/c58e03f3-6be4-439e-9356-58c52907935a)  
Para mejorar la productividad y el rendimiento de eslint te recomiendo que instales la extensión de ESLint, está disponible en los diferentes IDE "Entorno de Desarrollo Integrado" en mi caso VS Code.  
![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/28b10fc7-e2eb-4b46-bdc1-c0735607dd10)  


En algunos casos es necesario de desactivar algunas reglas de eslint que no son necesarias para aplicar en algunos de nuestros proyectos, esto lo podemos hacer en el archivo de configuración de eslint.   


![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/4170490a-9585-4004-8559-f3973533c5fb)    
En este ejemplo hay tres reglas desactivadas unas de TypeScript y otras de react.  

## Configurar Prettier 
Para configurar prettier en nuestro proyecto lo primero que debemos hacer es instalarlo para ello.  
### 1.	npm install --save-dev --save-exact prettier  
**2.**	Luego, creamos un archivo de configuración vacío para que los editores y otras herramientas sepan que está utilizando Prettier:  
**node --eval "fs.writeFileSync('.prettierrc','{}\n')"**  
Dentro de este archivo que se crea aplicamos las reglas que queremos que prettier aplique o desactive.  

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/84365111-f13b-4f03-aa6a-4ded8ff6fbd4)  
En este ejemplo tenemos desactivados los puntos y comas, las comillas simples son las que se aplican eliminando las dobles y comillas simples dentro del escope de jsx.   
También puedes tener instalado localmente en tu entorno la extensión de prettier y allí aplicar algunas reglas preestablecidas por defecto sin necesidad de tener instalado prettier en tu proyecto.  

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/b8241250-4379-433f-8284-4b828dc09876)  


para mejorar tu productividad puedes configurar tu editor de código en este caso será vscode para que al guardar te de formato al código, para eso debes de abrir la configuración json de vscode allí realizas algunos cambios, agregas las líneas de comando que te permiten al guardar dar formato.  

![image](https://github.com/luisfer738/Configuracion-de-ESLint-y-Prettier-en-un-proyecto-react/assets/90799388/ed3dc149-31a4-48c7-a507-2cdc0328f098)    
Para este caso tengo algunas reglas pre establecidas directamente en mi entorno, y agregada la configuración para JavaScript y TypeScript para el dar formato al guardar.  
## Evitar conflictos entre ESLint y Prettier
Si estás utilizando ESLint y Prettier en conjunto, sigue estos pasos para evitar conflictos:  
### 1. Usa `eslint-config-prettier`:  
Instala la configuración:  
**npm install --save-dev eslint-config-prettier**  
eslint-config-prettier es una herramienta que ayuda a evitar conflictos entre las reglas de formateo de ESLint y Prettier.  
Cuando estás usando ESLint y Prettier en el mismo proyecto, es posible que algunas reglas de ESLint entren en conflicto con el estilo de formateo que Prettier intenta aplicar. Por ejemplo, ESLint podría tener una regla que exige comillas dobles, mientras que Prettier prefiere comillas simples. Si ambos intentan corregir el código al mismo tiempo, podrían entrar en conflicto y dejar el código en un estado intermedio o causar errores.  
Aquí es donde entra **eslint-config-prettier:**    
**Desactiva Reglas Conflictivas de ESLint: eslint-config-prettier** desactiva todas las reglas de ESLint que están en conflicto con el formateo de Prettier. Esto asegura que Prettier y ESLint trabajen juntos de manera armoniosa.  
  **Integración Simplificada:** En lugar de ir regla por regla desactivando las que entran en conflicto con Prettier, puedes simplemente extender eslint-config-prettier en tu configuración de ESLint y se encargará de todo por ti.  
Para utilizarlo, después de instalar con **npm install --save-dev eslint-config-prettier**, agregarías **"prettier"** a la lista en la clave **`"extends"`** de tu archivo. **eslintrc.json o .eslintrc.js.**  
Por ejemplo:  
**json**    
**{** 
  **"extends": ["some-other-config-you-use", "prettier"]** 
**}**    
Al hacer esto, las reglas que conflictúan con Prettier se desactivarán, lo que te permitirá usar ESLint y Prettier juntos sin problemas.      
## 2. Usa `eslint-plugin-prettier`:  
**Instala el plugin:**    
**npm install --save-dev eslint-plugin-prettier**  
El paquete eslint-plugin-prettier sirve para integrar Prettier como una regla dentro de ESLint. De esta manera, puedes correr ESLint y obtener errores de formateo basados en las reglas de Prettier directamente en los resultados de ESLint. También te permite autocorregir dichos errores utilizando la opción **`--fix`** de ESLint.  
Al utilizar **`eslint-plugin-prettier`,** estás haciendo lo siguiente:  
**1. Integrar Prettier en ESLint:** En lugar de ejecutar Prettier y ESLint por separado, puedes ejecutar solo ESLint y obtener errores tanto de linting como de formateo en un solo paso.  
 **2. Unificar la corrección automática:** Al usar la opción **--fix** de ESLint, no solo corregirá problemas basados en reglas de ESLint, sino que también formateará el código según las reglas de Prettier.  
**3. Consistencia en el código:** Garantizas que todo el código cumpla con las reglas de linting y formateo, ya que ambos se manejan en un solo proceso.  
Para usar **eslint-plugin-prettier**, después de instalarlo con **npm install --save-dev eslint-plugin-prettier**, necesitarías realizar algunas configuraciones en tu archivo  **.eslintrc.json o .eslintrc.js**:  
## 1. Agregar "prettier" a la lista de plugin.  
 **Añadir la regla "prettier/prettier": "error"** para que se reporten los problemas de formateo como errores.  
**Ejemplo:**  
**json**  
**{**  
  **"plugins": ["prettier"],**  
  **"rules": {**  
    **"prettier/prettier": "error"**  
  **}**  
**}**  
Con esta configuración, cada vez que ESLint encuentre un fragmento de código que no cumpla con el formato establecido por Prettier, te lo señalará como un error. Si ejecutas ESLint con la opción `--fix`, intentará corregir automáticamente ese error de formateo.  
## 3. Verifica tu configuración:  
Revisa y ajusta tu configuración para evitar reglas contradictorias entre ESLint y Prettier.  
Siguiendo este tutorial, tendrás ESLint y Prettier trabajando armoniosamente en un proyecto react con TypeScript o JavaScript. 
# Configurar reglas de precommit con Husky  

Las reglas de precommit con Husky sirven para ejecutar tareas automáticas antes de realizar un commit. En este caso, la tarea es ejecutar ESLint para verificar que el código no tenga errores.  
El comando **npx mrm lint-staged** ejecutará el script **lint-staged** que se encuentra en el directorio raíz del proyecto. Este script es un hook de Git que se ejecuta antes de realizar un commit. El script usa la herramienta lint-staged para ejecutar ESLint en todos los archivos que han sido modificados o creados desde el último commit.  
Si ESLint encuentra algún error, el commit no se realizará. Se deberán corregir los errores antes de poder realizar el commit. Para garantizar que no se acepten commits con errores de ESLint, para instalarlo debemos de seguir los siguientes pasos:  
### 1. Ejecuta el siguiente comando:  
**npx mrm lint-staged** 
## 2. Instala Husky:  
**npm i husky --save-dev**   
Un desafío clave al trabajar en equipos es mantener la coherencia del código. Los "cambios fantasmas", que ocurren cuando diferentes desarrolladores tienen distintas configuraciones, pueden causar conflictos innecesarios. La solución a esto radica en establecer reglas comunes de formato.   
Personalizar y adaptar estas herramientas según las necesidades del proyecto es posible gracias a archivos de configuración como **`.prettierrc` y `.eslintrc`.** Además, para garantizar una cohesión entre ESLint y Prettier, se recomienda el uso de paquetes como **`eslint-config-prettier`.**    
La correcta configuración y uso de ESLint y Prettier en un proyecto React garantiza un código más limpio, coherente y libre de errores, facilitando la colaboración en equipo y la mantenibilidad del proyecto a largo plazo.  













# Design Tokens

Design Tokens son valores específicos que se utilizan para representar elementos de diseño en un proyecto. Estos valores incluyen colores, tamaños de fuente, márgenes, etc. y se utilizan para garantizar la consistencia visual en toda la aplicación.
Además, es una metodología, arquitectura de proceso que es agnóstico a la tecnología para que los productos escalen de forma sencilla.

## Ventajas y desventajas
- **Ventajas:**
    - Proporciona consistencia visual en toda la aplicación
    - Facilita el mantenimiento y actualización de los estilos
    - Mejora la colaboración entre diseño y desarrollo
    - Facilita la creación de temas y variaciones de estilo

- **Desventajas:**
    - Puede ser difícil de implementar en proyectos existentes
    - Puede requerir una curva de aprendizaje para el equipo
    - Puede requerir herramientas adicionales para automatizar el proceso

## Cómo funcionan
Los Design Tokens se definen en un archivo de configuración específico que es procesado por una herramienta de automatización, como Style Dictionary, Theo, Brand.ai, etc. Esta herramienta genera los archivos de estilos para diferentes plataformas a partir de los tokens de diseño.

## Cómo empezar a utilizar Design Tokens
1. Diseño y definición: Diseñar y definir el conjunto de tokens de diseño que se utilizarán en el proyecto.
2. Selección de la herramienta de automatización: Seleccionar una herramienta de automatización adecuada para el proy
3. Configurar la herramienta: Configurar la herramienta de automatización para conectarse al repositorio y especificar las reglas para generar los tokens.
4. Generar tokens: Utilizar la herramienta de automatización para generar los tokens y subirlos al repositorio.
5. Control de versiones: Utilizar una herramienta de control de versiones para gestionar y rastrear los cambios en los tokens.
6. Integración en el desarrollo: Integrar los tokens en el código de la aplicación mediante el uso de preprocesadores de estilos o herramientas de integración de tokens.
7. Integración en el diseño: Integrar los tokens en el proceso de diseño mediante el uso de herramientas de diseño.
8. Pruebas: Realizar pruebas para asegurar que los tokens se están utilizando correctamente.
9. Comunicación y documentación: Documentar y comunicar los tokens utilizados en el proyecto.
10. Integración y entrega continua: Utilizar una herramienta de CI/CD para automatizar el proceso de generar y subir los tokens al repositorio.
11. Mantenimiento: Continuar revisando y actualizando los tokens para asegurar la consistencia visual en toda la aplicación.

## Herramientas necesarias
- Herramienta de automatización: Style Dictionary, Theo, Brand.ai, etc.
- Control de versiones: Git, SVN, etc.
- Herramientas de integración: Preprocesadores de estilos, librerías de tokens, etc.
- Herramientas de diseño: Figma, Sketch, Adobe XD, etc.
- Herramientas de pruebas: herramientas de pruebas automatizadas, etc.
- Herramientas de documentación: JSDoc, etc.
- Herramientas de integración y entrega continua: Jenkins, Travis CI, etc.

## Pasos para conectar los tokens con el repositorio
1. Crear una nueva rama en el repositorio para los tokens.
2. Configurar la herramienta de automatización para conectarse al repositorio.
3. Generar los tokens y subirlos al repositorio.
4. Realizar un pull request para fusionar la rama de los tokens con la rama principal.
5. Realizar pruebas y verificar que los tokens se están utilizando correctamente en la aplicación.
6. Aceptar el pull request y fusionar los tokens con la rama principal.
7. Continuar actualizando y manteniendo los tokens en el repositorio.

## Consideraciones
- Es importante asegurarse de que todos los miembros del equipo entienden y utilizan los tokens correctamente.
- Es importante documentar y comunicar los tokens utilizados en el proyecto.
- Es importante realizar pruebas para asegurarse de que los tokens se están utilizando correctamente en la aplicación.
- Es importante continuar actualizando y manteniendo los tokens en el repositorio para asegurar la consistencia visual en toda la aplicación.
- Es importante considerar la escalabilidad y la portabilidad de los tokens al crearlos, para evitar problemas en el futuro.
- Es importante definir un proceso claro y documentado para la creación, actualización, y eliminación de los tokens.
- Es importante tener una comunicación constante entre el equipo de diseño y desarrollo para asegurar que los tokens estén alineados con las necesidades de ambos equipos.

## Ejemplo de un archivo de tokens en formato JSON
```JSON
{
  "colors": {
    "primary": "#00bfff",
    "secondary": "#f0e68c",
    "tertiary": "#ffd700"
  },
  "typography": {
    "base-font-size": "16px",
    "base-line-height": "1.5",
    "base-font-family": "Arial, sans-serif"
  },
  "spacing": {
    "base-unit": "8px",
    "small-unit": "4px",
    "large-unit": "16px"
  }
}
```
## Ejemplo de código para utilizar los tokens en un archivo CSS
```CSS
:root {
  --color-primary: #00bfff;
  --color-secondary: #f0e68c;
  --color-tertiary: #ffd700;
  --font-size: 16px;
  --line-height: 1.5;
  --font-family: Arial, sans-serif;
  --spacing-base: 8px;
  --spacing-small: 4px;
  --spacing-large: 16px;
}

.button {
  background-color: var(--color-primary);
  font-size: var(--font-size);
  line-height: var(--line-height);
  font-family: var(--font-family);
  padding: var(--spacing-base) var(--spacing-large);
}

.text {
  color: var(--color-secondary);
  margin-bottom: var(--spacing-small);
}
```
## Ejemplo de código para utilizar los tokens en un archivo JavaScript
```JS
const designTokens = {
  colors: {
    primary: "#00bfff",
    secondary: "#f0e68c",
    tertiary: "#ffd700"
  },
  typography: {
    baseFontSize: "16px",
    baseLineHeight: "1.5",
    baseFontFamily: "Arial, sans-serif"
  },
  spacing: {
    baseUnit: "8px",
    smallUnit: "4px",
    largeUnit: "16px"
  }
};

function createButton(text) {
  const button = document.createElement("button");
  button.textContent = text;
  button.style.backgroundColor = designTokens.colors.primary;
  button.style.fontSize = designTokens.typography.baseFontSize;
  button.style.lineHeight = designTokens.typography.baseLineHeight;
  button.style.fontFamily = designTokens.typography.baseFontFamily;
  button.style.padding = `${designTokens.spacing.baseUnit} ${designTokens.spacing.largeUnit}`;
  return button;
}

document.body.appendChild(createButton("Click me!"));
```

## Ejemplo de utilizar herramientas para la gestión de design tokens

### Configurar un archivo de tokens en formato JSON
```JSON
{
  "colors": {
    "primary": "#00bfff",
    "secondary": "#f0e68c",
    "tertiary": "#ffd700"
  },
  "typography": {
    "base-font-size": "16px",
    "base-line-height": "1.5",
    "base-font-family": "Arial, sans-serif"
  },
  "spacing": {
    "base-unit": "8px",
    "small-unit": "4px",
    "large-unit": "16px"
  }
}
```
## Se debe utilizar una herramienta como tokens-generator para generar archivos de estilos en diferentes lenguajes
```
npm install -g tokens-generator
tokens-generator tokens.json --output-css tokens.css --output-scss tokens.scss
```

## Se debeutilizar una herramienta como style-dictionary para generar archivos de estilos y tokens para diferentes plataformas
```
npm install -g style-dictionary
style-dictionary build
```

## Se debe utilizar una herramienta como Theme UI para utilizar los tokens en un proyecto de React

```
npm install theme-ui
```
```JS
import { ThemeProvider } from "theme-ui"
import theme from "./tokens.json"

function App() {
  return (
    <ThemeProvider theme={theme}>
      {/* Tu componente */}
    </ThemeProvider>
  )
}
```
## Ejemplo de código para conectar los tokens con un repositorio

### Se debe tilizar una herramienta como Git para versionar los archivos de tokens

```
git init
git add tokens.json
git commit -m "Initial commit"
```
## Utilizar una herramienta como Lerna para manejar múltiples paquetes en el repositorio y compartir los tokens entre ellos
```
npm install --global lerna
lerna init
lerna create @company/tokens
lerna add @company/tokens --dev
```

## Importar los tokens en un archivo de estilos
```
@import './tokens.scss';
```

## Utilizar los tokens en la definición de estilos
```CSS
.button {
  background-color: $color-primary;
  font-size: $font-size-base;
  padding: $spacing-base-unit;
}
```
## Utilizar los tokens en un componente de React
```JAVASCRIPT
import { useTheme } from 'emotion-theming'

function Button() {
  const theme = useTheme()
  return (
    <button style={{
      backgroundColor: theme.colors.primary,
      fontSize: theme.typography['base-font-size'],
      padding: theme.spacing['base-unit']
    }}>
      Click me
    </button>
  )
}
```
## Utilizar los tokens en un componente de Angular

```js
import { Component } from '@angular/core';
import { tokens } from './tokens.js';

@Component({
  selector: 'app-button',
  template: `
    <button [ngStyle]="{
      'background-color': tokens.colors.primary,
      'font-size': tokens.typography['base-font-size'],
      'padding': tokens.spacing['base-unit']
    }">
      Click me
    </button>
  `,
})
export class ButtonComponent {
  tokens = tokens;
}
```
## Importar los tokens en un archivo de estilos
```SASS
@import './tokens.scss';
```

## Utilizar los tokens en la definición de estilos

```CSS
.button {
  background-color: $color-primary;
  font-size: $font-size-base;
  padding: $spacing-base-unit;
}
```

## Utilizar los tokens en un componente de Vue
```html
<template>
  <div class="button">
    Click me
  </div>
</template>
```
```JAVASCRIPT
<script>
import { tokens } from './tokens.js'

export default {
  data () {
    return {
      tokens
    }
  },
  computed: {
    buttonStyles() {
      return {
        backgroundColor: this.tokens.colors.primary,
        fontSize: this.tokens.typography['base-font-size'],
        padding: this.tokens.spacing['base-unit']
      }
    }
  }
}
</script>
```
```HTML
<style scoped>
.button {
  background-color: tokens.colors.primary;
  font-size: tokens.typography['base-font-size'];
  padding: tokens.spacing['base-unit'];
}
</style>
```
## Utilizar los tokens en un archivo de configuración de Webpack
```JAVASCRIPT
const tokens = require('./tokens.js');

module.exports = {
  module: {
    rules: [
      {
        test: /\.scss$/,
        use: [
          {
            loader: 'sass-loader',
            options: {
              data: `$tokens: ${JSON.stringify(tokens)};`
            }
          }
        ]
      }
    ]
  }
}
```

## Conectar los tokens con el repositorio

- Utilizar una herramienta como style-dictionary para generar los tokens en diferentes formatos (por ejemplo, JSON, SCSS, JS, etc) a partir de un archivo de definición de tokens en formato YAML o JSON.

- Utilizar una herramienta de integración continua (CI) para automatizar la generación de tokens cada vez que se realiza un cambio en el archivo de definición de tokens.

-  Utilizar una herramienta de versionamiento (como Git) para controlar los cambios en el archivo de definición de tokens y en los archivos generados de tokens.

- Utilizar una herramienta de documentación (como Storybook) para documentar y mostrar los tokens y su uso en diferentes componentes y contextos.

- Utilizar una herramienta de automatización para documentar y mostrar los tokens y su uso en diferentes componentes y contextos.

# Figma-Tokens

Figma Tokens es una función en el diseñador en línea Figma que permite la creación y uso de elementos como colores, tipografías, espacios, bordes y otros valores de diseño de manera consistente a lo largo de un proyecto. Los Tokens se crean en una biblioteca compartida y se pueden utilizar en todas las páginas y componentes en un proyecto. Al cambiar el valor de un Token, se actualizará automáticamente en todas las apariciones en el proyecto. Esto mejora la consistencia del diseño y ahorra tiempo en la actualización manual de valores en varios lugares.

Ha sido creado por Jan Six

Documentación oficial: https://docs.tokens.studio/sync/github
Repo: https://github.com/six7/figma-tokens

# Integración de Figma Tokens en un proyecto

La integración de Figma Tokens en un proyecto permite tener una consistencia en el diseño y en el software, ahorrando tiempo y esfuerzo al no tener que actualizar manualmente los valores en varios lugares del proyecto.

## Generar archivos de configuración

Utilice herramientas como figma-tokens para generar archivos de configuración para diferentes lenguajes de programación, como JavaScript, SCSS, etc.

Por ejemplo, podemos utilizar tokens para establecer la tipografía en nuestro proyecto. Imaginemos que tenemos un token llamado "bodyText" que contiene la información de la fuente, tamaño y peso que debemos utilizar para el texto principal en nuestra aplicación.

```scss
@import './tokens.scss';

body {
  font-family: $bodyText-font-family;
  font-size: $bodyText-font-size;
  font-weight: $bodyText-font-weight;
}
```

Otro ejemplo podría ser el uso de tokens para establecer el espaciado entre elementos en nuestra aplicación. Imaginemos que tenemos un token llamado "spacing" que contiene el valor de espaciado en pixeles que debemos utilizar entre elementos.

```javascript
import { spacing } from './tokens.js';

const container = document.querySelector('.container');
container.style.marginBottom = spacing.m;
```

## Pasos para usar Figma Tokens con un proyecto usando Github

1. Crear un repositorio en GitHub
2. Añade un repositorio remoto
3. Inicia Figma Tokens en Figma
4. Ve los settings y elige GitHub y crea un nombre cualquiera
5. Crea un Personal Access Token en GitHub
6. Agrega el enlace a tu repositorio (ej. /sorangel/figma-tokens )
7. Indica la rama que usas por defecto (ej. main)
8. Crea el nombre del archivo json (ej. tokens.json)
9. Guarda y creo un mensaje en el primero commit de Figma tokens
10. Si todo está correcto debe haber creado un push en tu repositorio en Github

### Ahora debemos transformar los tokens a otro json que pueda ser leído por Style Dictionary

1. npm install token-transformer
2. npm install style-dictionary
    1. Esto crea automáticamente una carpeta tokens con un json dentro input.json
3. npx token-transformer tokens.json tokens/tokens.json
4. Crea un config.json
   ```JSON
   {
       "source": ["tokens/**/*.json"],
       "platforms": {
       "css": {
       "transformGroup": "css",
       "files": [
       {
       "destination": "css/variables.css",
       "format": "css/variables"
       }]
     }}
   }
   ```
5. Crea la carpeta css con un variables.css
6. Ejecuta: ```npx style-dictionary build --config config.json```
7. Crea tus scripts en package.json
```JSON
 "scripts": {
       "token-transformer": "token-transformer tokens.json tokens/input.json",
       "style-dictionary": "style-dictionary build --config config.json"
       }
```

##  API de figma 

El API de Figma es una interfaz de programación de aplicaciones (API, por sus siglas en inglés) que permite a los desarrolladores acceder y controlar recursos en Figma a través de solicitudes HTTP. Con el API de Figma, los desarrolladores pueden automatizar tareas, integrar Figma en sus flujos de trabajo y desarrollar aplicaciones personalizadas que se integren con Figma. Con el API, se pueden obtener información sobre los diseños y los componentes, actualizar y crear proyectos, y mucho más.

## ¿Comó se utiliza?
Para usar el API de Figma, es necesario tener una cuenta de Figma y crear una clave de API. Luego, se pueden realizar solicitudes a la API usando la clave de API y autenticarse con OAuth 2. Con el API de Figma, es posible obtener información sobre los diseños y proyectos de Figma, así como actualizar y crear elementos en tiempo real.

En resumen, para usar el API de Figma, los desarrolladores deben registrar una aplicación, autenticar a cualquier usuario, utilizar el token OAuth 2 y actualizar un token de OAuth 2. Luego, pueden realizar solicitudes a la API usando un lenguaje de programación compatible, como JavaScript o Python.

## Diferencias, ventajas y desventajas de usar el api de figma y el plugin Tokens Studio for Figma(Figma Tokens).

| Herramientas            | Diferencias                                                                                                                                                                                                                                                                                                                            | Ventaja                                                                                                                                                                                                                                              | Desventaja                                                                                                                                                                                                                                                                                                               |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| API Figma               | El API de Figma es una herramienta que permite acceder a los datos de una cuenta de Figma a través de una API RESTful.<br/> Con la API de Figma, es posible automatizar tareas como la recuperación de información de diseño, <br/>la creación y actualización de proyectos y la integración con herramientas externas.                | 1. Permite integrar Figma con otras herramientas externas. <br/> 2. Es posible automatizar tareas de diseño y desarrollo. <br/> 3. Ofrece una amplia gama de posibilidades y opciones para acceder y utilizar la información de una cuenta de Figma. | 1. Puede ser complejo de implementar para aquellos que no están familiarizados con el desarrollo de software. <br/> 3. Requiere un conocimiento técnico avanzado para utilizarlo de manera efectiva. <br/> 3. Es necesario tener una buena comprensión de la documentación y la API para poder utilizarla correctamente. |
| Tokens Studio for Figma | Tokens Studio for Figma es un plugin que permite gestionar y organizar los tokens de una cuenta de Figma. Con Tokens Studio for Figma, es posible crear, modificar y eliminar tokens, así como generar archivos de configuración para diferentes lenguajes de programación y aplicar automáticamente los tokens en toda la aplicación. | 1. Es más fácil de utilizar para aquellos que no tienen un conocimiento técnico avanzado.<br/> 2. Ofrece una interfaz intuitiva y fácil de usar.<br/> 3. Permite gestionar y organizar los tokens de una cuenta de Figma de manera eficiente.        | 1. No permite integrar Figma con otras herramientas externas. <br/> 2. No es posible automatizar tareas de diseño y desarrollo de la misma manera que con el API de Figma. <br/> 3. Ofrece menos posibilidades y opciones que la API de Figma.                                                                           |

## Links de Fuentes y documentación  

 [Design Tokens Community Group](https://www.designtokens.org/).
 [Design Tokens Format Module](https://tr.designtokens.org/format/).
 [Arcade](https://usearcade.com/).

### Desing Token Skeleton:

[Desing Token Skeleton-Figma](https://www.figma.com/file/IGr2xoqcZX91CU7CDr4ZsI/Design-tokens-(skeleton)?node-id=0%3A1&t=mj8M4qfDq8o2mpXH-0)
[Desing Token Skeleton-Repo-GitHub](https://github.com/klaufel/pattern-library-skeleton)

## ¿Que es lo principal que debe hacer el equipo de UI UX para comenzar a trabajar con design tokens ?

1.  Define los valores: Define los valores que representan tus marcas visuales y estilos, como colores, tamaños de fuente, espaciados, etc.

2.  Crea una biblioteca de tokens: Crea una biblioteca de tokens que incluya todos tus valores definidos. Puedes crear esta biblioteca manualmente o utilizar herramientas de software como Figma Tokens para ayudarte.

3.  Integra los tokens en tus proyectos: Integra los tokens en tus proyectos de diseño y desarrollo. Esto incluye utilizar los tokens en tus mocks y prototipos, así como en tus aplicaciones y sitios web.

4.  Documenta y comparte los tokens: Documenta y comparte los tokens con el equipo de diseño y desarrollo, para asegurarte de que todos estén alineados y utilicen los mismos valores en sus trabajos.

5.  Mantenimiento: Mantén y actualiza tus tokens regularmente para asegurarte de que sigan siendo relevantes y coherentes con los cambios en tu marca y estilo.

##  ¿Cuales son las herramientas que debe utilizar el equipo de UI/UX para empezar a trabajar con Design Tokens ?

Un equipo de UI/UX puede utilizar las siguientes herramientas para trabajar con Design Tokens:

1.  Figma Tokens: Herramienta de software para crear, almacenar y administrar tokens de diseño en Figma.

2.  Sketch Tokens: Plug-in de Sketch para crear y administrar tokens de diseño en Sketch.

3.  Style Dictionary: Herramienta de código abierto para crear, almacenar y administrar tokens de diseño en varios formatos y plataformas.

4.  Brand.ai: Plataforma de diseño de marca que incluye herramientas para crear, almacenar y administrar tokens de diseño.

5.  Adobe XD: Herramienta de diseño que incluye la capacidad de crear y administrar tokens de diseño.

6.  Microsoft Fluent: Herramienta de diseño de Microsoft que incluye tokens de diseño preestablecidos y la capacidad de crear y administrar tokens personalizados.
    
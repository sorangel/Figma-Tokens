# figma-tokens

Ha sido creado por Jan Six

Documentación oficial: https://docs.tokens.studio/sync/github
Repo: https://github.com/six7/figma-tokens

## Pasos para usar Figma Tokens con un proyecto usando Github

1. Crear un repositorio en GitHub
2. Añade un repositorio remoto
3. Inicia Figma Tokens en Figma
4. Ve los settings y elige GitHub y crea un nombre cualquiera
5. Crea un Personal Access Token en GitHub
6. Agrega el enlace a tu repositorio (ej. /DavidRivadeneyra/figma-tokens )
7. Indica la rama que usas por defecto (ej. main)
8. Crea el nombre del archivo json (ej. tokens.json)
9. Guarda y creo un mensaje en el primero commit de Figma tokens
10. Si todo está correcto debe haber creado un push en tu repositorio en Github

### Ahora debemos transformar los tokens a otro json que pueda ser leído por Style Dictionary

1. npm install token-transformer
2. npm install style-dictionary
    1. Esto crea automáticamente una carpeta tokens con un json dentro input.json
3. npx token-transformer tokens.json tokens/input.json
4. Crea un config.json
    1. {
       "source": ["tokens/**/*.json"],
       "platforms": {
       "css": {
       "transformGroup": "css",
       "files": [
       {
       "destination": "css/variables.css",
       "format": "css/variables"
       }
       ]
       }
       }
       }
5. Crea la carpeta css con un variables.css
6. Ejecuta: npx style-dictionary build --config config.json
7. Crea tus scripts en package.json
    1. "scripts": {
       "token-transformer": "token-transformer tokens.json tokens/input.json",
       "style-dictionary": "style-dictionary build --config config.json"
       }

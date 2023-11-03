# Aplicación de consola - Clean Architecture - MultiplicationApp

Es un proyecto de consola con principios o conceptos de arquitectura limpia, los temas que se ven son:

1. Funciones asíncronas auto-invocadas.
2. Banderas y opciones. 
3. `Yargs` y su configuración.
4. Instalación de dependencias (Versión específica, actual y futura).

### Para iniciar proyecto

1. Instalar las dependencias. 
```
npm install
```

2. Ejecutar la aplicación. 
```
npm run dev
```

### Anexo: Node con TypeScript (Inicio de proyecto)

1. Instalar `TypeScript` y demás dependencias.
```
npm i -D typescript @types/node ts-node nodemon rimraf
```

2. Inicializar el archivo de configuración de `TypeScript`.
```
npx tsc --init --outDir dist/ --rootDir src
```

3. Crear archivo de configuración `Nodemon` - `nodemon.json`
```
{
  "watch": ["src"],
  "ext": ".ts,.js",
  "ignore": [],
  "exec": "npx ts-node ./src/app.ts"
}
```

4. Crear scripts para `dev`, `build` y `start` en `package.json`.

```
  "dev": "nodemon",
  "build": "rimraf ./dist && tsc",
  "start": "npm run build && node dist/app.js"
```




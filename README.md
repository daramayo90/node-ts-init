# Node with TypeScript

1. Install TypeScript and other dependencies

```
npm i -D typescript @types/node ts-node nodemon rimraf
```

2. Init the typescript configuration file (can be configured as needed)

```
npx tsc --init --outDir dist/ --rootDir src
```

3. Create configuration file for Nodemon - nodemon.json

```
{
  "watch": ["src"],
  "ext": ".ts,.js",
  "ignore": [],
  "exec": "npx ts-node ./src/app.ts"
}
```

4. Create scripts for dev, build y start

```
  "dev": "nodemon",
  "build": "rimraf ./dist && tsc",
  "start": "npm run build && node dist/app.js"
```

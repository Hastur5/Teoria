1) crear el archivo mediante Vite
npm init vite@latest "titulo del archivo" -- --template react
npm init vite@latest e-commerce -- --template react (ejemplo)

2) npm install

3) npm i standard -D

4)agregar el ESlint con la guía de César.

"eslintConfig": {
    "extends": [
      "./node_modules/standard/eslintrc.json"  
    ]
  }

  5) agregar "import path from path" para sustituir los ../.. por @ en vite.config y después

  resolve: {
    alias: {
      '@': path.resolve(__dirname, './src')
    }
  }


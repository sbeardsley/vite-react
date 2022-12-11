npm create vite@latest my-react-app -- --template react-ts
cd my-react-app
npm install
npm i -D eslint
npx eslint --init
npx install-peerdeps --dev eslint-config-airbnb
npm i -D eslint-config-airbnb-typescript prettier eslint-config-prettier eslint-plugin-prettier   

in .eslintrc.cjs

replace 

```"eslint:recommended",``` 

with 

```
"airbnb",
"airbnb-typescript",
"airbnb/hooks",
```

add ```project: './tsconfig.json'``` to parserOptions:

in tsconfig.json

change include to this ```"include": ["src", ".eslintrc.cjs"],```
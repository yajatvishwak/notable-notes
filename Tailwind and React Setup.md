---
title: Tailwind and React Setup
created: '2020-08-27T08:29:38.442Z'
modified: '2020-08-27T13:44:44.466Z'
---

# Tailwind and React Setup 

How to get started with react app and tailwindcss support


## Create react app 
```
npx create-react-app appname
```


Test if app is running(Optional)
```
cd appname
yarn start
```

## Add tailwind, postcss, autoprefixer
```
yarn add tailwindcss postcss-cli autoprefixer -D
```


## Add the tailwind config file 
```
npx tailwindcss init --full
```

## Add the postcss.config.js file 
- import tailwindcss and maintain consistency of the css files
```
touch postcss.config.js
```
## Edit the postcss.config.js File
```js
//  postcss.config.js 
module.exports =  {
  plugins: [require('tailwind.css'), require('autoprefixer')] 
}
```
## Create a styles folder in src
- make the main.css and tailwind.css file
```
cd src
mkdir styles
cd styles 
touch main.css
tailwind.css
```

```
// Folder structure
---src
    |____ styles
              |____ main.css
              |____ tailwind.css

```

## Edit the tailwind.css
```
//tailwind.css
@tailwind base; 
@tailwind components;
@tailwind utilities;
``` 

## Edit the scripts in package.json
```js
//...

"scripts":{
  "start": "npm run build:css && react-scripts start", //<---- change this
  "build": "npm run build:css && react-scripts build", //<---- change this
  "test": "react-scripts test", 
  "eject": "react-scripts  eject",
  "build:css": "postcss src/styles/tailwind.css -o src/styles/main.css" // <---- add this
}

//...
```

## Import the styles/main.css file in all components (as such)

```js
// App.js 
import React from 'react';
import './styles/main.css';
function App() {
  return <div class="bg-green-600"> 
  Hello, from tailwind 🦄
  </div>

}
```



## 🎉 Setup Complete




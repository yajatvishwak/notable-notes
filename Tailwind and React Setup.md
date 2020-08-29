---
title: Tailwind and React Setup
created: '2020-08-27T08:29:38.442Z'
modified: '2020-08-29T07:17:01.088Z'
---

# Tailwind and React Setup 

How to get started with react app and tailwindcss support


## Create the react app
```
npx create-react-app appname
```

## Install tailwindcss, autoprefixer and postcss-cli  
```
npm install tailwindcss postcss-cli autoprefixer  --save-dev 
```

## Initialize your tailwind config file
```
npx tailwind init --full
```

## Initialize your postcss config file
```
touch postcss.config.js
```
## Add this to your postcss.config.js
```js
//postcss.config.js
 const tailwindcss = require('tailwindcss');
 module.exports = {
     plugins: [
         tailwindcss('./tailwind.config.js'),
         require('autoprefixer'),
     ],
 };

```

## Create a styles folder in src, which contains tailwind.css and index.css file
```
cd src && mkdir styles 
cd styles && touch tailwind.css index.css
```
## Edit the index.css
```css
//index.css
@tailwind base;
@tailwind components;
@tailwind utilities;
```
## Edit your package.json 
```js
"scripts": {
  "build:style":"tailwind build src/styles/index.css -o src/styles/tailwind.css",
  "start": "npm run build:style && react-scripts start",
  "build": "react-scripts build",
  "test": "react-scripts test",
  "eject": "react-scripts eject"
},
```
##  Delete the index.css and app.css files in your projects root directory and remove their corresponding import statements in both the Index.js and App.js files respectively.


## Using tailwind
```js 
import './styles/tailwind.css';
```




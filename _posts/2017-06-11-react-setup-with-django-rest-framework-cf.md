---
layout: post
title:  "Django REST with React: setting up React and webpack"
date:   2019-05-20 23:43:45 +0700
categories: [python, django, react, javascript]
---

The sweet spot for Django and React is Django REST framework for providing API endpoints.

With React in its own app called “frontend”.

We already know how to create a Django app so let’s do it again:

**Create A new app for React**


```console
django-admin startapp frontend
```

Let’s also prepare a directory structure for holding the React components:

```console
mkdir -p ./frontend/src/components
```
and the static files:

```console
mkdir -p ./frontend/{static,templates}/frontend
```

**Initialize NPM**

In the root folder of the project

```console
npm init -y
```

Next up install webpack and webpack cli with:

**Install webpack**

```console
npm i webpack webpack-cli --save-dev
```

Now open up package.json and configure the scripts:

```javascript
"scripts": {
  "dev": "webpack --mode development ./project/frontend/src/index.js --output ./project/frontend/static/frontend/main.js",
  "build": "webpack --mode production ./project/frontend/src/index.js --output ./project/frontend/static/frontend/main.js"
}
```

Save the file and close it

**Now let’s install babel for transpiling our code**
babel-plugin-transform-class-properties is necessary for using ES6 class static properties
```console
npm i @babel/core babel-loader @babel/preset-env @babel/preset-react babel-plugin-transform-class-properties --save-dev
```

**Pull in React and prop-types:**

```console
npm i react react-dom prop-types --save-dev
```

Inside the project root folder, create `.babelrc` file...

```javascript
{
    "presets": [
        "@babel/preset-env", "@babel/preset-react"
    ],
    "plugins": [
        "transform-class-properties"
    ]
}
```

And finally create a new file named `webpack.config.js` for configuring babel-loader:

```javascript
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: "babel-loader"
        }
      }
    ]
  }
};
```
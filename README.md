## Vue2project

### 初始化

安装npm, webpack, vue-cli等等全家桶工具。

`vue init webpack`命令，使用脚手架搭建一个初始化开发环境。会自动下载GitHub上的`template`项目，这是一个sample。本项目基于这个sample来进行组件上的添加等等操作，使它成为一个新的项目。

`npm start || npm run dev`用这两个命令来启动原始sample，注意这个命令会重新对所有代码进行打包编译等等，，访问[http://localhost:8080](http://localhost:8080)可以看到如下画面![vue-sample](https://i.imgur.com/mmhqZvR.png)

### Vue基本操作

`./build/build.js`将`process.env.NODE_ENV = 'production'`改为`process.env.NODE_ENV = 'development'`，注意是进入开发模式而不是生产模式。

- 入口：`./index.html`，这个文件基本不用改，也没什么东西，就是规定字符集和视图大小的，`<div id="app"></div>`这里面放了我们自定义的组件，不用改动，后期在其他文件中可以创建注册组件并使用。
- `./src/main.js`，这里主要是将`App.vue`这个组件注册并使用，注意这里使用了局部注册组件的方式，意思是必需要引入`import || require`组件才能使用；如果是全局注册，只需要直接使用就好了；更多关于组件注册的问题见[https://cn.vuejs.org/v2/guide/components-registration.html](https://cn.vuejs.org/v2/guide/components-registration.html "vue组件注册")
- `./src/App.vue`，这个文件使用了`<router-view>`这个组件，是全局注册的所以可以直接使用，router事实上是Vue官方的插件，在`./src/router/index.js`这个文件中引入了`HelloWorld`组件并注册，意思是在router中注册了，但`router-view`是全局注册的，所以使用`router-view`相当于使用`HelloWorld`组件。
- `./src/components/HelloWorld.vue`这个文件是一个单文件组件，由router引入，然后在App里使用。
- 一般来说都会自己写新的组件，写好一个`.vue`文件之后在App里直接引入，然后用局部注册的方式注册组件，最后在`<template></template>`使用这个组件。

### 单文件组件

单文件组件以`.vue`为后缀，模板语法可以是ES6 || CommonJS || typescript等等，有Babel之后都能编译成ES5；一般的单文件组件形如![vue单文件组件](https://cn.vuejs.org/images/vue-component.png)
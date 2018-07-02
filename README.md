# vue-element

> element-ui demo

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
全局安装vue-cli
vue init webpack 项目名
webstorm 安装vue.js 插件【plugin】,支持.vue文件语法

//element-ui 引入
完整引入
在main.js中引入
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';

按需引入
安装
npm install babel-plugin-component -D
修改.babelrc文件
_{
  "presets": [
    ["env",
    {
      "modules": false,
      "targets": {
        "browsers": ["> 1%", "last 2 versions", "not ie <= 8"]
      }
    }],
    "stage-2"
  ],
  "plugins": ["transform-vue-jsx", "transform-runtime"]
}_
修改为
_{
  "presets": [["es2015", { "modules": false }]],
  "plugins": [
    [
      "component",
      {
        "libraryName": "element-ui",
        "styleLibraryName": "theme-chalk"
      }
    ]
  ]
}_


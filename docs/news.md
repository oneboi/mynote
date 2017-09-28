# 新闻站




### 项目
用户登录注册页 

首页 

列表页 

详情页 

###  项目初始化

1. 文件中不可以有中文

2. 文件夹必须小写

3. vue  init webpack-simple projectname



###  做项目的基本思路

1. 规划组件结构
* Nav.vue 
* Header.vue
* Home.vue 
* Sidebar.vue

2. 编写对应的路由
 vue-router

3. 具体写每个组件功能
 

###  心得建议
1. 一些公共的文件比如（jquery文件引入）在index.html中引入
2. 注意路径
3. main中引入文件requrie() 或者import''






##  create project

```
vue init webpack-simple preoject 

```


### 需要的基本模块
vue-router 
vuex
axios

### css配置

>webpack2
webpack-simple  模板默认vue-loader，babel-loader，file-loader
需要使用css 必须下载和配置两个loader: style-loader和css-loader

```
安装
npm  install css-loader  style-loader -D


配置
webpack.config.js

{
        test: /\.css$/,
        loader: 'css-loader!style-loader',
        exclude: /node_modules/
 },
 
```



## 封装公共的组件比如loading效果

keep live  避免多次加载获取数据

光看是不行的 一定要去做做的很好很好 
看着简单，做起来会遇到很多问题 


## 目录
assets 静态资源目录
components


## 公用的东西

公用的组件 components 
公用的请求 requests
公用的函数 functions
公用的过滤器 filters
路由公用的router


http://blog.csdn.net/qq_38652603/article/details/73835153

在js中引入css 使用loader

>在index.html 或main.js中的引入 叫做全局引入 


@import '../assets/css/index.css'





## 书写组件的注意点 
后缀必须写
```
import  Navcomponent from './components/Nav.vue';
```

组件至少有一个标签
```
<template>
    
</template>

Failed to mount component: template or render function not defined.


```



## 路由

npm install vue-router -S

注意routes （配置选项）和router （注入选项）


mt30{
    margin-top:30
}


引入css 
@import '';引入css



## vuex 

在个人中心的时候 隐藏nav.vue 


1.从哪触发 app.vue  

```
取决于这个是否显示;
找一个变量来控制到底是消失还是隐藏

 <Navcomponent></Navcomponent> 

```


什么时候发起actions,路由变化的时候触发



>监听路由的变化

```
当路由变化时触发
 watch:{
    $route(to,from){
      alert(1)
    }
  }
```

```

to和from 都是对象
{name: undefined, meta: {…}, path: "/category", hash: "", query: {…}, …}

```

>多做几个项目自己一定可以很厉害的 



## axios 交互

$ npm  install axios -S



>axios 为什么好，因为他可以进行一些配置


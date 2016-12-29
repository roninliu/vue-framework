# vue-framework

----

VUE2.0开发模板，用于初始化项目。
主要使用包含：

 - vuejs 2
 - vuex 2
 - vue-router 2
 - Thinkjs 2

编译使用browserify，使用vueify解析vue模板，支持es6，7的JS写法，

###说明
默认为main模块下单页应用，如需要修改，请修改文件:
“ YouProjectPath/src/common/controller/error.js ”
文件第66行404Action代码如下：
```javascript
    //实现单页应用
    if (this.http.module === 'main' && !this.isAjax()) {
      let controller = this.controller('main/base');
      this.status(200);
      return controller.invoke('__call');
    }
    return this.displayError(404);
```
默认模块为：main，如果不是请自定义修改

###前端开发
前端开发目录为www目录下的src文件夹
如下：
![image_1b54mktu71cr216f1n2bsfq14g69.png-20.5kB][1]
  [1]: http://static.zybuluo.com/ronin/b1q86hp5uu6op9cy5zx4tfzs/image_1b54mktu71cr216f1n2bsfq14g69.png
  
文件夹说明：
- www ：前端开发主目录
- src ：vue开发目录
- static : 部署后可以访问目录
- api：用于获取后台数据交互
- common：公用方法，包括filters等
- comoponents：组合组件库，可以视为页面小模块
- widgets：单一功能组件，不涉及业务，纯前端组件
- router：路由
- store：vuex开发相关state，getter 模块等
- views：具体的页面
- bundle：自动编译文件
- lib：其他第三方库
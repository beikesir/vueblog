> **项目：vueblog**
>
> **公众号：MarkerHub**

### 介绍

一个基于SpringBoot + Vue开发的前后端分离博客项目，带有超级详细开发文档和讲解视频。还未接触过vue开发，或者前后端分离的同学，学起来哈。别忘了给vueblog一个star！感谢

### 技术栈：

![](https://oscimg.oschina.net/oscnet/up-4626cb696c003e36c4515e77adc7632c6ed.png)




### 项目文档：

开发文档：https://juejin.im/post/5ecfca676fb9a04793456fb8

**vueblog讲解视频：** https://www.bilibili.com/video/BV1PQ4y1P7hZ/



Fork：https://github.com/beikesir/vueblog项目vue前端部分学习

**1、克隆项目**

**2、装包：npm i**

**2.1、package.json**

package.json文件就是一个json对象；定义项目的配置信息、所需模块信息

一般字段解释：

name:项目名称

scripts:项目命令

dependencies:项目依赖项

devDependencies：开发阶段依赖项

**2.2、vue.config.js文件的通常作用**

vue.config.js是vue/cli项目的可选配置文件(vue/cli的全局配置保存在home下名为.vuerc的json文件)，会被@vue/cli-service自动加载；

也可以使用package.json中的vue字段代替本文件。

**3、运行：serve**



**4、permission.js文件被导入到main.js文件，相当于初始化了permission.js中的对象**

permission.js》router.beforeEach(()=>{})



**5、axios的使用**

1、导入axios：import axios from 'axios'

2、设置默认URL：axios.defaults.baseURL = "http://localhost:8081"



**6、vuex**

一般特性：全局单例模式集中存储和管理所有组件的状态



Vuex 应用的核心就是 store（仓库），包含应用中大部分的状态 (state)。

Vuex 和全局对象的不同？

Vuex 的状态存储是响应式的；通过显式地提交来改变装填。

创建

提供一个初始 state 对象和一些 mutation

操作

获取状态对象：store.state

触发状态变更：store.commit

Vue 组件中访问 this.$store property：以 store 选项的方式“注入”store



**7、简单的store 模式**

粗劣理解为低配版vuex。

var store = {

  debug: true,

  state: {

​    message: 'Hello!'

  },

  setMessageAction (newValue) {

​    if (this.debug) console.log('setMessageAction triggered with', newValue)

​    this.state.message = newValue

  },

  clearMessageAction () {

​    if (this.debug) console.log('clearMessageAction triggered')

​    this.state.message = ''

  }

}
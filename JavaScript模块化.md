# JavaScript模块化

[*js模块化历程*](http://www.cnblogs.com/lvdabao/p/js-modules-develop.html)


## CommonJS
CommonJS规范，一个单独的文件就是一个模块。
加载模块使用require方法，该方法读取一个文件并执行，
最后返回文件内部的exports对象
#### 定义模块
根据CommonJS规范，一个单独的文件就是一个模块。
每一个模块都是一个单独的作用域，在该模块内部定义的变量，
无法被其他模块读取，除非定义为global对象的属性
#### 模块输出
模块只有一个出口，module.exports对象，
我们需要把模块希望输出的内容放入该对象
#### 加载模块
加载模块使用require方法，该方法读取一个文件并执行，
返回文件内部的module.exports对象

[*CommonJS规范*](http://javascript.ruanyifeng.com/nodejs/module.html)

#### Browserify
https://github.com/substack/node-browserify#usage  
[*浏览器加载 CommonJS 模块的原理与实现*](http://www.ruanyifeng.com/blog/2015/05/commonjs-in-browser.html)  
[*通过 Browserify 在浏览器中使用 NodeJS 模块*](https://www.ibm.com/developerworks/cn/web/1501_chengfu_browserify/)  
[*Browserify：浏览器加载Node.js模块*](http://javascript.ruanyifeng.com/tool/browserify.html)  
[*前端模块及依赖管理的新选择：Browserify*](https://segmentfault.com/a/1190000002941361)

## AMD
AMD 是 RequireJS 在推广过程中对模块定义的规范化产出。  
[*ADM规范*](https://github.com/amdjs/amdjs-api/wiki/AMD)

```javascript
define("alpha", ["require", "exports", "beta"],
      function (require, exports, beta) {
      exports.verb = function() {
          return beta.verb();
          //Or:
          return require("beta").verb();
      }
  });
```
目前，实现AMD的库有RequireJS 、curl 、Dojo 、Nodules 等

#### requirejs
https://github.com/requirejs/requirejs  
https://github.com/amdjs/amdjs-api/wiki/require  
http://www.requirejs.cn/
#### curl
https://github.com/cujojs/curl  
http://cujojs.com/#get
#### dojo
https://github.com/cujojs/curl  
http://dojotoolkit.org/documentation/tutorials/1.10/hello_dojo/
##### nodule
https://github.com/kriszyp/nodules

## CMD
CMD 是 SeaJS 在推广过程中对模块定义的规范化产出。  
[*CMD规范*](https://github.com/seajs/seajs/issues/242)
```javascript
define(function(require, exports, module) {

   // 获取模块 a 的接口，调用模块 a 的方法
   var a = require('./a');  
   a.doSomething();

   // 异步加载一个模块，在加载完成时，执行回调
   require.async('./b', function(b) {
     b.doSomething();
   });

  // 对外提供 foo 属性
  exports.foo = 'bar';

  // 对外提供 doSomething 方法
  exports.doSomething = function() {};

});
```


#### seajs
https://github.com/seajs/seajs  
[*SeaJS与RequireJS最大的区别*](https://www.douban.com/note/283566440/)

## ES6（ECMAScript6、ES2015)

[*ECMAScript 6 入门*](http://es6.ruanyifeng.com/#docs/module)

#### ES5 和 ES6 浏览器支持情况
http://kangax.github.io/compat-table/es5/  
http://kangax.github.io/compat-table/es6/

#### babel
http://babeljs.cn/

## 标准对比
|标准|实现|优点|缺点|
|--|--|--|--|
|CommonJS|nodejs和browserify|便于重用、规范、易用、支持多|同步，不适合浏览器；不可以并行的非阻塞的加载多个模块|
|**AMD**|requirejs、curl、dojo、nodule|适合浏览器异步加载；可以多个模块并行加载；国外支持友好|不优雅|
|**CMD**|seajs|并行异步加载；兼容nodejs|需要spm打包，逻辑偏重|
|ES6|babel|容易进行静态分析；面向未来的es标准|原生的浏览器还没有支持；新版的nodejs才支持|

## 补充
#### CSS模块化
http://www.jianshu.com/p/d46bc8cf3afa
#### 整体模块化
http://fex.baidu.com/blog/2014/03/fis-module/  
http://saito.im/note/The-Architecture-of-F2E/  
http://zhizhi.betahouse.us/2015/10/24/qian-duan-mo-kuai-ji-yi-lai-guan-li/

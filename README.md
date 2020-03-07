# FrontPref
前端性能优化

## HTML优化

渲染顺序

- 1、CSS样式表置于头部，CSS会一边加载一边渲染
- 2、JS脚本置于尾部，JS在未加载完成之前，会阻塞渲染
- 3、使用外部的样式表和脚本，优先加载出HTML结构
- 4、关键JS、CSS代码可以内嵌在HTML中，比如：rem动态等
- 5、避免使用iFrame
- 6、使用骨架屏


## CSS优化

加载优化
- 1、避免使用css的@import
- 2、避免使用通配符
- 3、避免使用!impotant
- 4、优化css reset，项目中不会用到这么多reset
- 5、避免使用css表达式

动画优化
- 1、可以使用transform开启图形加速
- 2、用translate取代left，可以避免页面重排

选择器优化
- 1、选择器嵌套尽量不要超过三层
- 2、id选择器尽量不要嵌套
- 3、使用继承

体积优化
- 1、提取公共CSS


## JS优化

运行速度

- 1、如果没有兼容问题，尽量使用原生方法
- 2、根据兼容浏览器的最低版本，考虑是否使用polyfill
- 3、switch语句相对if，可以较快通过将case语句按照最可能到最不可能的顺序进行组织
- 4、位运算较快。当进行数字运算时，位运算操作要比任何布尔运算或者算数运算快
- 5、巧用||和&&布尔运算符，可以减少执行代码语句
- 6、使用加号拼接是最快的，其次是String()、.toString()、new String()
- 7、需要使用定时器时，用setTimeout取代setInterval，setInterval会一直占用内存
- 8、制作JS动画时，使用requestAnimationFrame取代setTimeout和setInterval

变量优化

- 1、避免全局查找，可以将需要访问的属性用变量保存
- 2、使用变量比使用对象属性和数组元素要快
- 3、对于包含大量数据而不需要操作的对象，可以使用Object.freeze冻结对象，加快运行速度

减少无用操作

- 1、使用节流、防抖
- 2、使用事件委托取代大量事件的绑定
- 3、若需要对DOM进行大量操作，可以使用Fragment减少操作次数

减少未使用代码

- 1、进行tree-shaking，删减未使用的代码

算法优化

- 1、添加key值，最大效益的使用虚拟DOM，减少Diff时间
- 2、使用benchmark测试不同算法的性能，择优


## 网络优化

请求数量上限：

- 1、每个网站最多允许同时6个请求，可以考虑将资源分类部署

请求速度优化：

- 1、使用CDN，可以加速资源的请求速度

加载时间分配：

- 1、核心资源预加载

- 2、大体积资源按需加载（Webpack拆包）

减少加载体积

- 1、压缩图片
- 2、压缩HTML、CSS、JS代码
- 3、开启网络压缩，如：GZIP

减少加载次数

- 1、制作精灵图
- 2、将小图片转换为base64字符串
- 3、使用浏览器缓存
- 4、使用前端缓存，如: LocalStorage、Cookie、SessionStorage等
- 5、减少重定向请求，比如：nginx反向代理的重定向
- 6、避免使用服务端字体


## React性能优化

1、优化react事件，避免使用闭包函数

2、使用持续化数据结构Immutable对redux进行管理

3、优化`shuoldComponentUpdate`生命周期定义基础组件BaseComponent取代React.Component

4、使用纯组件PureComponent

5、添加Key值


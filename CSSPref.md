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

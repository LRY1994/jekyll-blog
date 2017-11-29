# myPersonalSite
Inspired by some blogs made by their own host ,I decide to make one of myself.Record my life !

### 安装Jekyll
http://www.jianshu.com/p/1093b5565918
按照里面的步骤我遇到一个问题：jekyll new 的时候提示
> could not load bundler, bundler install skip.

解决方法: gem install jekyll bundler

jekyll官网
https://jekyllrb.com/

 Liquid template language
 

### 关于scss
所有的sass导入文件都可以忽略后缀名.scss。一般来说基础的文件命名方法以_开头，如_mixin.scss。这种文件在导入的时候可以不写下划线，可写成@import "mixin"。

sass的导入(@import)规则和CSS的有所不同，编译时会将@import的 ``scss ``文件合并进来只生成一个CSS文件。
但是如果你在sass文件中导入 `` css `` 文件如@import 'reset.css'，那效果跟普通CSS导入样式文件一样，导入的css文件不会合并到编译后的文件中，而是以@import方式存在。

sass有两种注释方式，一种是标准的css注释方式/* */，另一种则是//双斜杆形式的单行注释，不过这种单行注释不会被转译出来。

** sass的变量必须是$开头 **，后面紧跟变量名，而变量值和变量名之间就需要使用冒号(:)分隔开（就像CSS属性设置一样），如果值后面加上!default则表示默认值。变量作为属性或在某些特殊情况下等则必须要以#{$variables}形式使用
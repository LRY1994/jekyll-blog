# myPersonalSite
Inspired by some blogs made by their own host ,I decide to make one of myself.Record my life !

### 安装Jekyll
http://www.jianshu.com/p/1093b5565918
按照里面的步骤我遇到一个问题：jekyll new 的时候提示
> could not load bundler, bundler install skip.

解决方法: gem install jekyll bundler

### 关于scss
所有的sass导入文件都可以忽略后缀名.scss。一般来说基础的文件命名方法以_开头，如_mixin.scss。这种文件在导入的时候可以不写下划线，可写成@import "mixin"。

sass的导入(@import)规则和CSS的有所不同，编译时会将@import的 ``scss ``文件合并进来只生成一个CSS文件。
但是如果你在sass文件中导入 `` css `` 文件如@import 'reset.css'，那效果跟普通CSS导入样式文件一样，导入的css文件不会合并到编译后的文件中，而是以@import方式存在。

## _layout 和 {{content}}
刚开始有点疑惑，他就是类似于局部替换那样，{{content}}指的就是那个使用这个layout的文件的内容

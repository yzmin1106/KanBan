KanBan
======

`KanBan`是我和`FuLei39`童鞋正在为S项目的持续集成工作开发的看板，所谓`看板`，就是在引人注目之处摆一大屏幕，不停滚动显示一些持续集成的相关信息，很拉风，很装B！

当前版本基于一个`jQuery`的[模板](http://tympanus.net/codrops/2013/05/07/a-collection-of-page-transitions/)改动而来，基本可以使用了

大致介绍：

1. 打开`index.html`文件，里面内嵌了3个`iframe`，每个`iframe`指向一个我关注的持续集成页面，例如：`Jenkins`页面、单元测试报表、SVN提交日志，等
2. 当然，每次只显示其中一个页面，不同页面之间以`15s`为间隔定时自动切换，所有页面以`60s`为间隔定时刷新
3. 点击`下一页`切换
4. `Please download and have a try!`

但是，`KanBan`可以做得更多、更好！

我期望中的`KanBan`应该是这样的（草图）：

![看板草图](https://raw.github.com/chenkan/KanBan/master/ued/KanBan.png)

1. `上一页`按钮，功能不解释
2. `下一页`按钮，功能不解释
3. `指定页`按钮，这其实是个下拉框，可以前往任意页面
4. `暂停/继续`按钮，功能不解释
5. `立即刷新`按钮，功能不解释
6. 除此以外，工程根目录下有一个`config.js`文件，我希望在这里可以以`key - value`对的形式存储想访问的页面，例如：`网易首页 - http://www.163.com`；每次打开`KanBan`，就从里面读取配置，从而访问指定页面；草图中的`当前iframe的描述`就是这个`key`
7. 当然，还希望`页面切换时间`和`刷新时间`也可以在`config.js`中配置

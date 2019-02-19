### ~
- 本项目仓库仅仅用于记录学习过程和技术讨论

### 目前能用的程序：
- 一个简单的shell脚本，可以定时调用scrapy_news.py维护数据库
- 一个简单的爬虫脚本（scrapy_news.py），里面只有两个方法，一个是初次爬取数据，一个是每天维护数据库数据的方法。现在爬的是六十多个文章栏目，视频栏目的爬虫还没写（逻辑是一样的，先实现其他部分）。
- 导出了一个文章的数据库，一共有一万七千多条文章，供需要的童鞋使用

### 剩下的工作：
- 这几天写好rest风格的后台接口。
- 再用python的GUI写一个桌面应用，这个桌面应用可以拿到每天最新的新闻数据，然后自动调用浏览器去执行（使用自动化测试框架实现），并且不会重复观看，除此之外就是一些搜索功能。
- 方案一：提供定时自动登录（云主机上程序用selenium框架拿二维码+拿到后用ssh协议传输到树莓派+树莓派上的appium-server执行扫码动作），登陆后自动观看不重复的文章（selenium打开文章页面，并且每次都需要滑到文章的底部+mysql记录看过的文章，已经实现了），但是搭建appium需要主机支持虚拟化，而云主机是禁用虚拟化的，所以这个方案不适合傻瓜化操作。
- 方案二：分析api和js，构造请求函数，这样就可以用wxpy框架把这一套程序移植到微信公众号上了。（感觉提前去做这个会很干扰其他部分的进度，毕竟构造请求是个靠脑子和运气的事）
- 方案三：在ubuntu上搭个selenium的环境（有的看比较舒服），写个python脚本并不结束进程，每天定时执行观看文章和视频的动作。只要webdriver不退出登陆是不会失效的。

### 目前状态
- 桌面端程序api开发中
- **技术渣渣、龟速开发**

### 开发速度
- 边学边做，缓慢开发

### 开发理念
拥护党的纲领，遵守党的章程，履行党员义务，执行党的决定，严守党的纪律，保守党的秘密，对党忠诚，积极工作，为共产主义奋斗终身，随时准备为党和人民牺牲一切，永不叛党。

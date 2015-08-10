# MEIPIC
这是一个开源的Android图片浏览器.
开源的基于实时的html解析,主要内容为图片加文字贵,不基于服务器,是一个独立的本地项目.
该项目通过实时的分析html,动态的加载出列表,标题,和内容以及图片.
该项目适配了android5.0系统,目前为基础版本,存在一些bug,欢迎大家修改并提出一些建议.
对爬虫项目、Android5.0项目有兴趣的网友可以下载学习.
该项目所解析的网址为天极图片网,未获得授权的个人或者公司,请勿用于商业用途.仅供于学习.郑重提醒,误用于商业用途,里面的网址可自行修改.


对该项目的展望,其实该项目爬取的规则是使用dom解析,由于图片网站的中html的规律性,可以很容易的分析出我们所需要的内容.

   所以我们可以让用户定义出常用的图片网站列表的解析规则,比如列表解析的规则是".mainClass div ul li a",这样我们很容易的就找到class是mainClass标签下的
div中的ul中的li中a标签,这样列表的所在的href超链接就获取到了,然后我们需要看此列表中的内容时可以再解析该列表的内容,与解析列表的
方法是一样的.

    基于此,我们可以在该项目中添加一个侧滑的菜单,里面有用户自己定义的需要解析的网址的列表(点击可进入具体网站解析后的结果),这里可以有一个添加按钮,点开后进入
添加界面,里面有网站的网址,列表的解析规则的填写,列表中内容解析规则的填写,每个列表中内容中特定元素的解析规则的填写(这些规则的填写统一用dom解析的方式,
不清楚dom选择规则的童鞋可自行百度非常简单),通过这种方式用户可以自定义需要解析的网站的,增加选择性.


    我们扩展性再高一点,可以引入云端存储(可以引入评论,点赞等功能,根据url匹配的方式)的用户自定义的功能,用户添加自定义网址时可以
(1)选择其他网友上传到云数据中的自定义的网址(包含解析规则)(这里可以有一个单独的页面,用户选择网友的自定义),
(2)也可以选择手动添加自定义的网址以及规则,当用户调试解析过后显示正常时,长按侧滑栏中该条目可以选择上传至公共的数据库或者是私人的数据库.
    
    这样我们一个有史以来最强大的图片浏览器就构建成功了(还可以加入别的,例如搞成在线的图书浏览器,或者是阅读的,不仅仅是图片,还可以是视频,音乐).
如果我们用户量足够大,我们甚至可以让网站他们自己上传他们的解析规则,或者更强的是网站本身做的过程中去匹配我们定义的规则,比如列表的class必须等于list,或者自创别的标签(例如<div mplist="fds"/>).
    
    我们还可以把规则网址打包成一种格式的文件,用户用我们的app打开文件就询问是否添该网址.如果假如聊天的功能,就能够更加方便.
如果我们再扩展,比如有图书或者电影音乐,网站他们可以在列表中添加标记,需要密码才能进入来收费,或者是登录,购买,把该app做成一个超级强悍的平台,未来的另一个互联网的船票,超越微信,作为一个入口,还可以加入离线浏览的功能.

我只是写了一个最基本的东西,未来还需要靠大家扩展升级.

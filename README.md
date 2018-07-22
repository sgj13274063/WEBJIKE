# Hello World
欢迎使用小呆导航源码，这一个非常棒的开始.

使用它你可以快速搭建一个专属你自己的多分类导航跟博客，源码采用了较宽松的MIT开源协议，你只需保留版权声明，就将此模板用于商业用途、也可以随意修改源码，生成自己的一套模板。

>**注意！小呆导航后台只支持.NET平台，即Windows操作系统**

# 站在巨人的肩膀上 #
**小呆导航基于SiteServer CMS免费开源内容管理系统制作而成**

在使用它之前，请先下载做好以下准备：

- 已经安装好了IIS6.0或以上版本；

- 已经安装好了.net framework 4.5.2或以上版本；

- 已经安装好了MySql、Sql Server、PostgreSQL或Oracle四种数据库的任何版本；

- 下载SiteServer CMS系统安装包；官网：http://www.siteserver.cn/

安装步骤只会介绍重要的部分，详细教程请自行百度或查看官方操作文档：http://docs.siteserver.cn/getting-started/#/

# 本地环境部署 #
官方文档已经写得非常详细，就不作搬照了：http://docs.siteserver.cn/getting-started/#/how-to-install-siteserver-cms

网站后台安装完成后，访问地址登录：http://localhost:99/siteserver/login.aspx

- 1.创建空站点（不使用站点模板）

- 2.站点名称随意；站点级别：子站；文件夹名称：随意；其他选项默认即可；

- 3.1进入网站后台》系统管理》站点管理》站点模板管理》导入站点模板（选择下载好的源码压缩包）

>*注意！站点模板压缩包必须是T_开头，且压缩内不能再嵌套文件夹，否则导入模板会出错*

- 3.2如果嫌导入模板的方式较麻烦，可以先解压网站模板压缩文件，文件夹名称同样是以T_开头，然后将文件夹拷贝进该目录：siteserver_install\SiteFiles\SiteTemplates

- 3.3刷新网站后台，进入系统管理》站点管理》站点模板管理，即可看到导入的网站模板

- 4点击模板右边的“创建站点”，站点名称就是你网站的名称；站点级别：主站；其他选项默认即可

- 5此时网站创建完毕，点击“站点链接》访问站点”查看网站效果，同时你也可以去“系统管理>站点管理”里面删除掉前面创建的子站

# 网站内容更新 #
> *注意！由于网站内容绝大部分都是静态html页面，意味着你更新某个了页面后需要重新生成该页面（博客/文章页面除外）*

- 网站所有的内容更新都在“信息管理》内容管理”里面操作，想更新哪个页面的内容，只需进入对应的栏目即可。

- 增加新页面、新导航页、新目录都在“信息管理》栏目管理”里创建

## 修改LOGO
LOGO图片尺寸为50 * 50px，默认是旋转状态，将你的LOGO图片文件放到站点根目录的“images”文件夹里面，替换掉“logo.png”文件即可；参考路径：G:\siteserver_install\images

若不想LOGO旋转，打开“显示管理》样式文件管理》style.css”文件，注释或删掉85~155行代码

## 修改网站名称和标语
设置管理》站点设置》站点属性
> 注意：此页面的内容每次修改都需要重新生成所有页面

## 修改网站底部信息及统计代码
显示管理》包含文件管理》footer.html

统计代码需要你去友盟+官网注册一个账号，复制你的统计代码覆盖原来默认的统计代码

- 由于首页没有网站底部信息，所以需要去首页模板文件中修改并生成首页文件：显示管理》模板管理》系统首页模板；拉到页面底部，“回到顶部”div下面的两行代码就是统计代码，替换掉即可。

>此文件修改完成后，同样需要重新生成所有页面

## 修改评论系统
为了使留言内容可移植的需求，小呆导航使用了第三方评论系统“畅言”。开源版本的网站模板评论系统同样是使用了畅言，为了能正常演示，默认使用了小呆导航的畅言安装代码，所以你看到你的网站评论内容其实是和小呆导航的评论内容是一致的。

请自行注册账号获取安装代码，畅言官网：http://changyan.kuaizhan.com/

**在线留言页面**
- 显示管理》模板管理》在线留言；将你的畅言安装代码替换58~65行代码，然后生成该页面即可

**博客文章页面**
- 显示管理》模板管理》博客正文；将你的畅言安装代码替换79~81行代码，注意sid="{content.Id}"不能修改，否则会导致所有文章的评论内容都是一样的。
>修改模板后需要生成“个人博客”栏目下所有内容页面，而不是只生成“个人博客”栏目页

## 修改网站简介：关于本站
- 站点管理》栏目管理》关于本站
简介内容就和文章一样写就对了，样式随意自定义；修改完成后，选中“关于本站”栏目》生成该栏目页

## 写博客
- 站点管理》内容管理》个人博客》添加

**基础**

标题：文章标题；副标题：无用.留空；图片：文章封面图片（不需要图片就留空）；视频：用不上.留空；附件：用不上.留空

内容：这里是文章正文，爱写什么随你

内容摘要：可留空（文章无封面图片时，建议写内容摘要）

作者：文章作者，必填项（当然，你不填一样能发布）；来源：无用.留空


**其他**

属性：暂时只对“置顶”和“推荐”有用，其他两个选项无效果，“推荐”的文章会在个人博客右列表显示

标签：给文章打上标签，引用次数多的标签会在个人博客右列表显示

其他选项无需填写，保持默认即可

## 发布教程资源
>开源版本的网站模板之所以会保留“教程资源”这个栏目，是希望各位能分享一些可能对别人有用的教程资源

发布方式同上面发表文章差不多，若默认分类不适用，可到“信息管理》栏目管理》教程资源”中删改/添加

- 封面图片建议尺寸：428*280px

- 附件选项是资源的下载链接

## 更新导航链接

导航链接分两种：首页和行业导航；发布入口为：信息入口》内容管理》首页导航 和 信息入口》内容管理》导航目录

**首页导航**

> 首页导航每个模块（栏目）最多可放9个链接，每个模块请勿上传超过9个内容

- 标题：网站名称
- 其他》外部链接：网站url

**行业导航**

- 标题：网站名称

- 副标题：网站描述

- 图片：网站图标

- 其他》外部链接：网站url

**行业导航 创建分类**

>每个子分类都是一个栏目，每个子分类下可以放无数个链接，前端版导航的“视频教程”分类就是一个栏目，这个分类可以上传所有关于视频教程类的网站

在前端版导航中创建一个“图片素材”分类为例：

+ 信息管理 》 栏目管理 》 添加栏目

+ 父栏目：导航目录 》 前端开发；栏目名称和栏目索引相同，其他选项保持默认

+ 图标Class：从http://fontawesome.dashgame.com/ 中获取，粘贴对应图标的类名即可

+ 锚链接索引和锚链接ID：索引以#开头，内容和锚链接ID一致，如：#row-1 | row-1（注意：同个分类下的锚链接不能重复）

+ 确定，完成分类创建

## 修改favicon图标

进入网站根目录直接替换favicon.png文件即可

## SEO优化

SEO优化只需针对网站所有的栏目页做处理即可，所有内容页的SEO会自动获取，网站标题“内容标题 | 网站名称”、关键字“同上级栏目关键字一致”、描述“同上级栏目描述一致”。

设置入口：信息管理 》 栏目管理， 编辑对应栏目即可


- 栏目内容：网站名称（例：小呆导航  - 可自定义的简洁网址导航）

- 关键字列表：页面的关键字（例：小呆导航,网址导航,前端导航,设计师导航,CG导航,工作导航,自定义导航,简洁导航,网站大全）

- 页面描述：页面的描述（例：小呆导航是一个可自定义的简洁多领域网址导航，收录了前端开发、设计师、影视后期、日常办公等领域优质网站，为广大用户提供高效率的上网导航服务。）

> 提示：SEO设置只需针对3级以上目录，3级以下的栏目无需设定，因为3级目录没有独立页面。如：首页 》 导航目录 》 前端开发 》 视频教程，这个目录就属于4级目录，所以无需设置SEO信息，因为视频教程这个分类在网站中是不会独立显示的。


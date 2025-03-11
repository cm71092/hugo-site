+++
date = '2025-03-09T21:50:00+08:00'
draft = false
categories = ["技术"]
title = '成功部署完网站的喜悦'
tags = ["生活记录", "感想"]
description = "简单记录一下做博客的体会"
+++

![封面图](/cover.png)
## 我终于能点开自己的博客啦！
> ~~在失败了数十次之后~~，我终于成功点开自己的博客啦！！

我基本上是跟着ds来做的，但是中途就转战stack主题官方帮助文档和gpt了，体感下来ds能够辅助完成一些**大方向**的工作，比如提供建立一个博客的方案，但是具体到每一步怎么做的时候，ds就会出错，我在前几次跟着ds走的时候，基本上步骤就是缺斤少两的，所以怎么也打不开自己的网站的😭

后来我先是去网上搜了下别人是怎么用ds给的方案做博客的，又是给gpt发我的错误日志报告，最后终于成功建立了现在这个博客！一开始本地服务器一切显示正常，我准备push到我的github仓库的时候还有点紧张，害怕报错，不过我push的过程非常顺利，等待了一两分钟，就可以在同一个局域网里通过网站链接访问我的博客啦~🥰

## 一点心得体会
首先放上我的config.toml文件：

```

theme = "hugo-theme-stack"
baseURL = "https://cm71092.github.io/"
languageCode = "zh-cn"
hasCJKLanguage = true
title = "老二刺螈的博客小站"
DefaultContentLanguage = "zh-cn"

[pagination]
pagerSize = 5


[params]
  description = "这是我的网站"
  defaultDark = false  # 日间模式为默认
  mainSections = ["post"]
  favicon = "favicon.ico"
  
  [params.footer]
  since = 2025   

  [params.dateFormat]            # 🌟日期格式
  published = "Jan 02, 2006"     # 发布日期格式（Go时间格式）
  lastUpdated = "Jan 02, 2006 15:04 MST"  # 最后更新格式              

  [Params.Sidebar]
    subtitle = "暨大光电研究牲，二刺螈爱好者"
    emoji = "🥰"

    [params.sidebar.avatar]
      enabled = true
      src = "img/avatar.png"  
      local = true

[[params.widgets.homepage]]      # 首页小部件列表
type = "search"                  # 搜索框

[[params.widgets.homepage]]
type = "archives"                # 归档列表

  [params.widgets.homepage.params]
  limit = 5                      # 显示5条最新归档

[[params.widgets.homepage]]
type = "categories"              # 分类云

  [params.widgets.homepage.params]
  limit = 10                     # 显示前10个分类

[[params.widgets.homepage]]
type = "tag-cloud"               # 标签云

  [params.widgets.homepage.params]
  limit = 10

[[params.widgets.page]]
type = "toc" 

[taxonomies]
  category = "categories"
  tag = "tags"


[menu]
main = [ ]

  [[menu.social]]
  identifier = "github"
  name = "GitHub"
  url = "https://github.com/cm71092"

    [menu.social.params]
    icon = "brand-github"

  [[menu.social]]
  identifier = "bilibili"
  name = "Bilibili"
  url = "https://space.bilibili.com/13107588"

    [menu.social.params]
    icon = "bilibili"

  [[menu.social]]
  identifier = "知乎"
  name = "知乎"
  url = "https://www.zhihu.com/people/tao-zi-98-90-73"

    [menu.social.params]
    icon = "zhihu"

[related]
includeNewer = true
threshold = 60
toLower = false

  [[related.indices]]
  name = "tags"
  weight = 100

  [[related.indices]]
  name = "categories"
  weight = 200

[markup.goldmark.extensions.passthrough]
enable = true

  [markup.goldmark.extensions.passthrough.delimiters]
  block = [ [ "\\[", "\\]" ], [ "$$", "$$" ] ]
  inline = [ [ "\\(", "\\)" ] ]

[markup.goldmark.renderer]
unsafe = true

[markup.tableOfContents]
endLevel = 4
ordered = true
startLevel = 2

[markup.highlight]
noClasses = false
codeFences = true
guessSyntax = true
lineNoStart = 1
lineNos = true
lineNumbersInTable = true
tabWidth = 4    

```

基本上是按照stack主题官方给的config文件来的，不过有两点需要注意：
+ 新版hugo把config文件名字修改为了hugo
+ 大部分主题的高版本只支持.toml后缀的config文件
> 其实意思就是要把主题官方给的config.yaml文件转成hugo.toml

说实话这两个问题真的困扰了我很久！我前几次尝试失败基本都是因为这两个问题，解决了这些之后我的博客创建非常简单，只需要根据示例文件里的格式按自己想法增减各个组件就行了。

还有个问题也是有点整蛊，就是hugo这个服务器老是乱缓存东西😡，有时候我明明修改了东西，但是就是刷新不出来，搞得我又是问ds又是问gpt，乱改了一通东西破大防。~~结果第二天重新打开服务器自己就加载出来了~~







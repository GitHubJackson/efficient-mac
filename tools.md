## 写在前面

各有所好，各取所需，love & peace

> 点击对应的工具名称，可以到达下载页面，大部分页面需要翻墙访问，建议先安装科学上网软件，推荐 [Xiyou](https://xiyou4you.us/r/?s=16659178)

## mac 辅助工具

- [Alfred](https://www.alfredapp.com/)。mac 神器不用多说，可以快速搜索文件和打开应用等
- [Xnip](https://apps.apple.com/cn/app/xnip-%E6%88%AA%E5%9B%BE-%E6%A0%87%E6%B3%A8/id1221250572?mt=12)。截图工具，可以在桌面放置多个悬浮截图
- [licecap](https://www.macupdate.com/app/mac/49461/licecap)。录屏工具，可以录取指定屏幕范围的活动、生成 Gif
- [Keka](https://www.keka.io/en/)。解压缩工具
- [Xiyou](https://xiyou4you.us/r/?s=16659178)。稳定的科学上网软件，要收费，支持多端

## 浏览器

- [chrome](https://support.google.com/chrome/answer/95346?hl=zh-Hans&co=GENIE.Platform%3DDesktop)

## 包管理工具

- [homebrew](https://brew.sh/)。安装 Git、nvm、node 等

> 官网的方式可能会安装不了，可以参考下搭建环境里面介绍的方法：https://github.com/GitHubJackson/efficient-mac/blob/master/frontend-dev.md

## 命令行工具

- [iterm2](https://iterm2.com/)。当前 mac 最好用的终端工具
- [oh my zsh](https://ohmyz.sh/#install)

> 安装过程如果遇到这个问题： Failed to connect to raw.githubusercontent.com port 443:Connection refused，试试给网络的 DNS 配置加一个 114.114.114.114

### zsh 插件

基本安装思路是进入插件目录，将插件拷贝到这个目录

```
cd ~/.oh-my-zsh/plugins
git clone [插件仓库]
```

然后在 `~/.zshrc` 文件中修改代码

```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search) // 空格间隔
```

- [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting.git)。高亮命令行

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

- [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions.git)。自动补全命令行

```
git clone https://github.com/zsh-users/zsh-autosuggestions.git
```

- [web-search](https://github.com/sinetoami/web-search.git)。快速 google、百度等

```
git clone https://github.com/sinetoami/web-search.git
```

> 也可以尝试用另一个 https://github.com/lesonky/web-search, 这个还支持知乎、mdn 等搜索

不过貌似都还不支持搜索中文内容 emmm，提了 issue，看看后续有没有办法解决：https://github.com/sineto/web-search/issues/3

- [autojump](https://github.com/wting/autojump.git)。快速跳转到路径

```
git clone https://github.com/wting/autojump.git
```

> 其他插件可以在这里找：https://github.com/unixorn/awesome-zsh-plugins

## 前端开发相关

- [vscode](https://code.visualstudio.com/download)。编辑器
- [sublime Text](https://www.sublimetext.com/3)。轻量级编辑器
- [Dash](https://kapeli.com/dash)。离线技术文档
- [charles](https://www.charlesproxy.com/download/)。网络代理工具
- [postman](https://www.postman.com/)。api 调试工具
- Git。版本控制工具，建议通过 homebrew 安装
- node。前端必备的运行环境，包括 npm，建议通过 homebrew 安装
- nrm。管理 git 源，比如 taobao、cnpm...建议通过 npm 全局安装
- nvm。管理 node 版本

### 数据库管理

- [MongoDB Compass](https://www.mongodb.com/try/download/compass)

## 待办事项工具

- [滴答清单](https://dida365.com/about/download)。UI 美观、操作方便、账号同步，个人感觉蛮好用的一款清单软件

## 笔记

- [有道云笔记](https://note.youdao.com/download.html)。云盘共享
- [Notion](https://www.notion.so/desktop)。功能很强的一款笔记软件，包括清单、日历、表格等功能

## 画图

- [draw.io](https://github.com/jgraph/drawio-desktop/releases)。流程图、时序图等
- [processon](https://www.processon.com/)。和 draw.io 类似，UI 更美观些，不过免费空间很小
- [xmind](https://www.xmind.cn/download/)。思维导图

## office

- [wps office](https://www.wps.cn/)

## chrome 插件

- FEhelper
- Octortree
- 沙拉查词
- Clear Cache。快速清理网页缓存
- Website IP
- SimilarWeb。测网站流量来源及相关信息
- Dark Reader
- React Developer Tools
- NIM。node 调试工具
- 下载+
- GitZip for Github。方便下载 github 仓库文件
- 股票基金助手。股市有风险

> 建议登录谷歌账号同步设置

## vscode 插件

- Todo Tree
- GitLens
- Auto Rename Tag
- open in browser
- Bracket Pair Colorizer 2
- ES7 React/Redux/GraphQL/React-Native snippets
- Material Theme
- Material Theme Icons
- Path Autocomplete
- koroFileHeader。生成文件头部注释和函数注释
- Paste JSON as Code。能快速生成 JSON 数据的 ts 数据类型

> 建议登录 vscode 同步设置

## 云存储

- [Google 云盘](https://drive.google.com/drive/my-drive)。免费空间 15G，不下载视频啥的，应该够用了，而且不限速(emmm，我并没有在暗示什么)...
- [百度网盘](https://pan.baidu.com/download?from=header#pan)

## 网站

- [AST](https://astexplorer.net/)
- [Babel](https://babeljs.io/repl#?browsers=defaults%2C%20not%20ie%2011%2C%20not%20ie_mob%2011&build=&builtIns=false&corejs=3.6&spec=false&loose=false&code_lz=Q&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=env%2Creact%2Cstage-2&prettier=false&targets=&version=7.15.3&externalPlugins=&assumptions=%7B%7D)
- [quicktype](https://app.quicktype.io/)。可以快速生成对象的数据类型，支持多种语言，比如 typescript
- [codesandbox](https://codesandbox.io/)。网页版编辑器，内置了很多模板
- [FreeSSL](https://freessl.cn/)。免费生成 SSL 证书
- [Pexels](https://www.pexels.com/zh-cn/)。大量免费的素材图片
- [carbon](https://carbon.now.sh/)。生成代码片段截图，蛮好看的，可以用在自己的文章里面
- [xml-sitemaps](https://www.xml-sitemaps.com/)。帮助生成网站的 sitemap
- [favicon](https://tool.lu/favicon/)。制作 favicon

## FTP

- [FileZilla](https://filezilla-project.org/download.php?type=client)。比较流行的 FTP 软件，有远程服务器的童鞋可能需要

## 其他

- 微信
- QQ
- 网易云音乐
- 搜狗输入法。手机、pc 共享剪切板，有点香 ~
- [keyManager](https://keymanager.org/)。证书管理工具，配合 FreeSSl 使用
- [JustFocus](https://getjustfocus.com/)。休息一会、或者专注工作一会

## 写在前面

emm，大部分插件都是要翻墙下载的，搜索建议用 google（某度广告是真的多，而且很多知识也需要翻墙才能看），建议先解决这个问题，毕竟都 2021 了，程序员不翻墙说不过去

> 推荐 Xiyou，用了几年，很稳定，性价比也可以了：https://xiyou4you.us/r/?s=16659178

## shell

可以把 shell 理解成 操作系统内核外的一层壳，它是用户和操作系统交互的桥梁，后来 shell 也慢慢地变成了内核与用户交互的脚本语言的总称，比如：bash、zsh、csh、ksh、ash 等等。

```
// 查看支持的 shell
cat /etc/shells
```

常见的 shell 命令如下：

```js
~(
  // 表示当前用户根目录，比如 ~/.zshrc
  pwd
); // 显示当前目录
cd; // 跳转至目录
ls; // 列出当前目录下的文件及文件夹
mkdir; // 新建文件夹
touch; // 新建文件
mv; // 移动文件
rm - r; // 删除文件，-r 参数表示递归删除目录
echo; // 打印字符串或变量
cat; // 输出文件内容
vim; // 编辑文件内容
source; // 执行某一个文件，比如 zshrc 修改之后要生效，可以通过这个命令 source ~/.zshrc，或者重开一个窗口
```

### iterm2

了解了 shell，我们还需要一个终端来输入 shell 命令和查看命令执行结果。mac 下最好用的终端当然是 iterm2 了，官网安装即可：https://iterm2.com/

### oh my zsh

目前 macOS 最流行的 shell 脚本语言应该就是 zsh 了。默认的 zsh 配置很繁琐，可以通过 `oh my zsh` 更好地体验 zsh

> 通过官网提供的命令行安装 oh my zsh：https://ohmyz.sh/#install
> 安装过程如果遇到这个问题： Failed to connect to raw.githubusercontent.com port 443:Connection refused，试试给 Wifi 的 DNS 配置加一个 114.114.114.114

## homebrew

可以通过官网提供的命令行安装，不过我一直安装失败，提示如下：

```
fatal: unable to access 'https://github.com/Homebrew/brew/': LibreSSL SSL_read: SSL_ERROR_SYSCALL, errno 60
Failed during: git fetch --force origin
```

搜了其他解决方案，比较多的是使用中科院的镜像，不过前提是先安装 Git，不过我没参考这个，感觉有点麻烦，具体可以去 google 搜下；我用的是国内的源

```
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```

> 具体解决方案参考：https://gitee.com/cunkai/HomebrewCN

> homebrew 使用指北：https://sspai.com/post/56009

## nvm / node

通过 nvm 管理 node 版本（包括 npm）

```
brew install nvm
```

安装完会提示到 `~/.zshrc` 文件中补充 nvm 命令的配置，可以通过 vim 编辑 `~/.zshrc` 保存

```
nvm install stable // 安装最新稳定版 node
node -v
npm -v
```

> nvm 常用命令可以参考这个文章，整理的还可以：https://titangene.github.io/article/nvm.html
> 当然，你可以直接上 Github：https://github.com/nvm-sh/nvm

## Git / nrm

日常开发最常用的版本控制工具，有时候也会通过 `Git` 下载一些第三方包，比如 zsh 的一些插件等。然后 `nrm` 主要是用来管理 git 源，比如 taobao、cnpm、企业源...

```
brew install git
npm i -g nrm // 要先安装 node
nrm use taobao // 我一般选taobao源
```

## 远程连接

### 必备

- 申请服务器，比如 [腾讯云](https://curl.qcloud.com/q3nCBH0x)、[阿里云](https://www.aliyun.com/activity/ambassador/share-gift/goods?taskCode=shareNew2108&recordId=null&userCode=4ta4u3yh)...个人网站一般 1 核 2g 就够用了，操作系统的话推荐使用 centos7.6 系统
- 用户名和 IP 地址
- 账号和密码

### 连接

ssh 连接远程服务器的过程是这样的：

1. 用户服务器发起登录请求：ssh user@IP
2. 服务器收到用户的登录请求，把自己的公钥发给用户
3. 用户使用这个公钥，将登录密码加密后，发送回远程主机
4. 服务器用自己的私钥，解密登录密码，如果密码正确，就同意用户登录

假设你已经买了一台 Linux 主机，IP 地址 为 x.x.x.x，用户名为 root （大部分默认为 root），使用以下命令可发起建立 ssh 连接：

```
ssh root@x.x.x.x
```

接下来输入密码登录即可

也可以通过 sshKey 实现免密码登录

```
brew install ssh-copy-id
// 生成本机密钥/公钥文件
ssh-keygen -t rsa
// 将本机公钥上传到远程服务器上
ssh-copy-id root@x.x.x.x
```

iterm2 设置快捷登录服务器，步骤参考：

1. 打开 `iterm2 -> preferences -> Profiles`，或者快捷键 `command + ,`
2. 点击左侧列表下的 + 号，新建一个 Profile
3. 右边配置相关信息，主要是配置 command，在初始化该窗口时自动执行连接服务器的命令

```
// Command
ssh root@x.x.x.x
```

之后右键点击 iterm2，就可以快速创建一个连接远程服务器的窗口了

## 总结

以上就基本搭建好一个前端开发环境了，后续有新的内容会继续补充，欢迎大家提 issue

## 其他

新用户使用优惠购买很划算哦！

- [腾讯云服务器限时优惠](https://curl.qcloud.com/q3nCBH0x)
- [阿里云服务器优惠券](https://www.aliyun.com/activity/ambassador/share-gift/goods?taskCode=shareNew2108&recordId=null&userCode=4ta4u3yh)

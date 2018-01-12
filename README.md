# Less


## 怎样学习？

> [官网](http://lesscss.org/)
> [中文网](http://lesscss.cn/)
> http://www.w3cplus.com/css/less

## 编译less文件

### 通过node.js编译

#### 1、安装node

在当前目录有个node-v5.2.0-x64.msi文件，双击其进行安装。此演示安装到c盘根目录。

#### 2、简单使用node

在nodejs目录下按住shift键加鼠标右键空白处会出现右击菜单，其中有一项是在“此处打开命令窗口”可以直接打开命令窗口，并自动将路径转到当前目录下。
![Alt node-install-path](https://github.com/c-jian/Git/raw/master/img/node-install-path.png)

Node命令：
```shell
node.exe -v   nodejs的版本
npm -v  npm版本

```
![Alt node-use](https://github.com/c-jian/Git/raw/master/img/node-use.png)

#### 3、配置环境变量

在桌面右击计算机属性->高级系统设置->高级->环境变量->PATH->加上node.js路径，路径与路径之间用英文分号隔开
![Alt system-path](https://github.com/c-jian/Git/raw/master/img/system-path.png)

以上完成如有问题，尝试重启explorer
![Alt explorer](https://github.com/c-jian/Git/raw/master/img/explorer.png)

#### 4、安装lessc

使用npm安装
```shell
npm install -g lessc
```

安装完成后会在下面目录出现三个文件夹[这个位置是默认的全局目录]
![Alt npm-global-path](https://github.com/c-jian/Git/raw/master/img/npm-global-path.png)
![Alt see-lessc-number](https://github.com/c-jian/Git/raw/master/img/see-lessc-number.png)

#### 5、编译less文件

通过cd命令将less文件路径引入，使用lessc编译，此时会在当前less文件目录下编译好css文件

注：如果路径间有空格，切换的时候要用双引号包含路径
![Alt compile-less](https://github.com/c-jian/Git/raw/master/img/compile-less.png)

lessc中c代表compile编译

如果我想将编译后的文件放到指定目录呢？
![Alt save-path](https://github.com/c-jian/Git/raw/master/img/save-path.png)

大于号 [ > ] 右边指定编译到哪里
此时将编译好的css文件引入html中即可。

### 使用less.js在浏览器动态编译

此方法无需引入css文件，只需引入less文件，然后在body结束标签前引入less.js通过Ajax向服务器请求进入编译。所以这种方法需要在服务器环境下进行，并且在线编译需要时间。

注：此方法可以用在开发阶段，或演示。当开发完成再一次性编译完成，然后引入css文件。这样就可以在开发阶段直接编写less文件，省事又省时。
![Alt less.js](https://github.com/c-jian/Git/raw/master/img/less.js.png)

具体演示在当前目录下的less.js下

### 使用Koala软件动态编译

#### 安装koala

koala.exe在当前目录下

#### 打开选择less文件目录

![Alt koala](https://github.com/c-jian/Git/raw/master/img/koala.png)

点击less文件，然后点编译，再刷新，就可以在less目录下也会有css文件了，此后就在less文件写，在html文件引入css文件，当less文件更新，软件会自动更新css文件里的内容。
![Alt koala-use](https://github.com/c-jian/Git/raw/master/img/koala-use.png)

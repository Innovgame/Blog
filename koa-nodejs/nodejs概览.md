# Node.js

> 2019.08.31 

## node常见模块，可以应用的场景

* web聊天室(`Socket.io`)
* web博客(`Hexo`)
* web论坛(`Node Club`)
* 前端模块管理平台(`Bower.js`)
* 浏览器环境工具(`Browserify`)
* 命令行工具(`Commander`)
* web服务器框架(`Express`  `Koa` `Meteor` `Egg`)

## Node安装

> 省略 

## NPM

> NPM 是一个JavaScript的`模块管理工具`，遵循`CommonJS`规范， Node 中自带的包管理工具
>
> 地址： [npm](www.npmjs.com)

### npm命令

查看`npm`帮助

> ```bash
> npm help
> ```
>
> ```bash
> npm <command> -h     quick help on <command>
> npm -l           display full usage info
> npm help <term>  search for help on <term>
> npm help npm     involved overview
> npm adduser -h
> ```

### NPM模块结构

完全符合CommonJS规范的模块应该包含以下文件

* package.json 模块的描述文件
* bin 存放可执行的二进制文件
* lib 存放JavaScript代码
* doc 存放文档
* test 存放单元测试文件

### package.json

> 通过`npm init`创建 package.json中包含了模块所有的依赖关系，详细的各个字段的详细解释: [package.json解释](https://docs.npmjs.com/files/package.json)

一个简单的package.json

```json
{
  "name": "koa-test",
  "version": "1.0.0",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "description": "",
  "dependencies": {
    "koa": "^2.8.1"
  }
}
```

### node_modules

| Input        | Command       | Output       |
| ------------ | ------------- | ------------ |
| package.json | `npm install` | node_modules |

### Other

> 另一款新的Node包管理工具 `Yarn`

## NVM

> 方便切换node版本 

详细安装使用参考：[nvm使用](https://github.com/nvm-sh/nvm)

## npm上发布模块

* 首先需要在npm官网上注册一个账号

* 命令：

```
npm publish
```



## 工具

* web代理工具NProxy 
  * 跨平台，支持但文件，多文件及目录替换，支持http，https 协议的web代理工具，在文件替换功能上尤其出色
  * [npm地址](https://www.npmjs.com/package/nproxy)


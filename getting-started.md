# 快速上手

## 要求
- [Node.js][1] v5.0或以上
- npm v3.0 或以上([不了解npm?][2])
- 配置好的文本编辑器([如何配置编辑器?][3])

## 开始

## 1. 运行`npm install`

这个命令会根据项目中的`package.json`文件安装项目依赖及开发工具
注: 由于众所周知的原因,从npm官方下载会碰到些问题,最好是将npm仓库源替换成淘宝镜像
```bash
npm config set registry https://registry.npm.taobao.org
npm config set disturl https://npm.taobao.org/dist
```

## 2. 运行`npm start`

这个命令会对`/web/src`的文件编译到`/web/assets`中，并监视`/web/src`中的文件变动，在初始化的编译完成后会启动BrowserSync,它会在你修改`/web/src`中的文件后自动刷新页面

> http://localhost:3000 BrowserSync服务器(需先启动PHP服务器)
> http://localhost:3001 BrowserSync控制面板


BrowserSync的代理地址为`http://localhost:8000`,如需修改代理地址或服务器端口号,请到`/gulpfile.js`中找到下面这段代码:
```javascript
browserSync({
    host: 'localhost',
    port: 3000,
    proxy: 'http://localhost:8000'
  });
```
选项说明:
- host: BrowserSync服务器的主机名
- port: BrowserSync服务器的端口名
- proxy: 代理地址

## 3. 其它

构建生产环境代码:
`npm run build`

检查 css 和 js 语法错误和潜在的问题:
`npm  run lint`



  [1]: http://nodejs.org
  [2]: http://www.ruanyifeng.com/blog/2016/01/npm-install.html
  [3]: https://github.com/w3cay/ushopal-style-guide/blob/master/config-text-editor.md

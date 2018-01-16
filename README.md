## vue-ghpages-test

> 测试gh-pages包的自动化发布

## how to use

1. 工程下安装gh-pages的包 `npm install gh-pages --save`
2. package.json 文件中配置npm scripts

  ```bash
  "scripts": {
    "dev": "webpack-dev-server --inline --progress --config build/webpack.dev.conf.js",
    "start": "npm run dev",
    "build": "node build/build.js",
    "deploy": "gh-pages -d dist" ## 添加部署选项
  },
  ```

3. vue 项目执行 `npm run build` 生成打包后的文件，**注意**发布到github gh-pages分支的话需要保证打包路径,也就是修改 config/index.js 中的 build对象的assetsPublicPath: './'

4. 执行 `npm run deploy` 命令，输入github 帐号密码，开始部署。

## 关于gh-pages 包

[gh-pages](https://github.com/tschaub/gh-pages)

1.该项目可用于打包vue项目；生成桌面可执行文件和安装包；目录为build
<!-- 2.直接将vue项目打包出的static等资源文件复制进dist目录；执行npm run build即可 -->
2.直接加载项目对应地址，执行npm run build
3.打包信息可自定义，修改package.json中的"build": {}部分
4.如果出现打包成的安装包或执行文件打开是白屏的情况；可能是vue项目打包的资源有问题
    vue cli2中可能是config下的index.js的build:{} 部分的assetsPublicPath有问题；可以改成'./'试试
    cli3之上可能是vue.config.js中的公共路径有问题。
    正常情况下vue打包出的index.html可以直接使用（或者在服务器上可以使用）
5.本项目由官网项目改编  
打包前需要下载eletron：
6.依赖安装
    1.安装electron
        npm install electron
    2.安装electron-builder
        npm install electron-builder
    3.可能需要将
    "dependencies": {}中的"electron-builder"，移到"devDependencies":{}中
    4.至此，正常情况下可以正确打包了！
7.也可以直接执行
    npm install electron --save--dev
    npm install electron-builder --save--dev
    只是这样会更改package.json，在打包的时候可能会将依赖打包进去
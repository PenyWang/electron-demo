## npm包安装注意事项
1. mac 
   1. 打开terminal。运行 vi ~/.npmrc
   2. 添加 electron_mirror="https://npm.taobao.org/mirrors/electron/"
2. windows 
   1. 打开cmd，执行以下命令
    ``` js
    npm config set ELECTRON_MIRROR "https://npm.taobao.org/mirrors/electron/"
    npm config set ELECTRON_CUSTOM_DIR "{{ version }}"
    ```
3. 执行npm i或yarn add 安装项目依赖即可

## 打包流程注意事项
1. windows打包
   1. 需要在package.json的package选项中将项目路径及输出路径改成自己本机的路径
   2. 打包命令
      ``` js
      yarn run build
      yarn run pack:win
      ```
2. mac 打包
   - 打包命令
   ``` js
      yarn run build
      yarn run pack:mac
   ```

## 开发启动electron
1. 实时热更新
   ``` js
   yarn run start
   yarn run electron:dev
   ```
2. 采用build后的静态文件
   - 此方式更接近真实环境，但不适合频发操作
   ``` js
   yarn run build
   yarn run electron:pro
   ```
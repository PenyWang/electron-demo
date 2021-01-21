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
1. 需要在package.json的package选项中将项目路径及输出路径改成自己本机的路径
2. 打包命令
   ``` js
   npm run build
   npm run package
   ```
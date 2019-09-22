# 闲云旅游后台

> 闲云旅游管理后台 / API接口

## 安装

```
npm install 
```

或者用`yarn`

```
yarn install
```



## 启动

```
npm run start
```



## API文档

### 安装apidoc

```
npm install apidoc -g
```

### 生成文档

```
apidoc -i docs -o apidoc
```

打开根目录的`apidoc`文件夹的`index.html`查看`api`文档



## 数据库

根目录下的`.temp/data.db`是`sqlite`数据库表，可以下载`DB Browser (SQLite)`工具打开该文件。

<https://sqlitebrowser.org/>

> 可以打开sqlite数据库的软件很有很多，可以自行搜索

## github第三方登录
+ github第三方登录需要配置redirect_uri
+ 故要修改后台代码中`api>account>Account.js line17`对应前端项目上线的地址以及github后台配置的地址。
+ 账号gz-itcast密码adad001122.
+ 登录github之后，点击小头像点击设置->最右侧选择最后开发者设置（Developer Settings）
+ 选择OAuth Apps
+ 选择闲云旅游
+ 注意： **第一次授权之后，后续使用github登录不会再跳转到github页面询问授权信息，而是直接返回，如果想要清除授权，点击Revoke all user tokens按钮即可**
+ 并修改**Homepage URL**和**Authorization callback URL**的地址为前端项目部署地址即可